import pyotp, time

# Secret key (The QR that's shared between you & the server)
secret = pyotp.random_base32()

#generate the 6 digit code (we're using a package because I'm lazy)
totp = pyotp.TOTP(secret)

print("Secret:", secret)
print("Current 2FA code:", totp.now())

# Wait 30s and you'll get a new code
time.sleep(30)
print("Next code:", totp.now())
