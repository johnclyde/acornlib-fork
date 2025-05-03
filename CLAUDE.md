This code is tricky, because it uses Acorn, a programming language that you don't know.

Acorn is a theorem proving language. Look at real.ac and nat.ac to get a sense of how it works.

# Verification

To verify the code, use one of the following commands depending on system setup:
```
# If verify is in your PATH
verify

# Or using relative path to the Acorn repository
../acorn/target/release/verify

# Or using absolute path (adjust as needed)
/path/to/acorn/target/release/verify
```

This command checks if all the theorems in the codebase are valid according to the Acorn theorem prover.
