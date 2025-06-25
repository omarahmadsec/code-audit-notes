# 🔐 Flask Login Review – Insecure Auth Handling

## Target

```python
@app.route('/login', methods=['POST'])
def login():
    user = db.find_user(request.form['email'])
    if user and request.form['password'] == user.password:
        session['user'] = user.email
        return redirect('/dashboard')
    return 'Login failed'
```

##🔥 Issues Identified

    ❌ Passwords stored and compared in plaintext

    ❌ No rate limiting or brute-force protection

    ❌ No password hashing or salting

    ❌ User input not sanitized or validated

##💥 Exploitation

    Attacker could brute force passwords using automated scripts

    An insider leak of the DB would expose real passwords

    Missing CSRF protection could allow forced login attempts

##🛡️ Fix Suggestions

    Use werkzeug.security.check_password_hash() and store hashes

    Add rate limiting with Flask-Limiter

    Validate input and use CSRF tokens

    Consider integrating Flask-Login for session hardening
