# Experiment 3: Challenge-Response Authentication and Replay Attack Handling

### Aim :-

To implement challenge-response authentication using a random nonce and shared secret, and detect replay attacks.

### Context/Theory :-

Challenge-response authentication allows a client to prove its identity without sending the secret directly. The server provides a random challenge, and the client uses it with the shared secret to generate a response. Reusing an old response can lead to a replay attack.

### Methodology :-

The server generates a random nonce and sends it as a challenge. The client combines the challenge with the shared secret to create a response. The server then verifies the response. A used challenge is stored so that its reuse can be identified as a replay attempt.

**Tools and Techniques:** Python 3, VS Code, `hashlib`, `secrets`, SHA-256, nonce generation, and replay detection.

### Procedure :-

1. Define a shared secret key.
2. Generate a random challenge using `secrets`.
3. Generate the client response using the challenge and secret.
4. Verify the response on the server.
5. Store the used challenge.
6. Reuse the challenge to simulate a replay attack.
7. Detect and reject the reused challenge.

### Result :-

Authentication was successfully performed, and reuse of the same challenge was detected as a replay attack.

### Discussion :-

A random nonce makes each authentication challenge different. Keeping track of used nonces helps prevent the same challenge from being accepted again.

### Improvement :-

One-time nonce tracking was added to detect and prevent reuse of an old challenge.

### Conclusion :-

The experiment demonstrated challenge-response authentication and basic replay attack detection using a nonce and shared secret.
