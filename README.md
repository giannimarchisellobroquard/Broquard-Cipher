
Broquard Cipher – Core Protocol Mechanics
How it works – engineered for absolute operational dominance:

Every operator generates a private SenderChain: a 32-byte root key drawn directly from os.urandom — true cryptographic entropy, no compromises.
The chain advances relentlessly with every message using BLAKE2b as the KDF. Each transmission derives a fresh, unique symmetric key. No key reuse. Ever.
Sender keys are securely distributed to peers exclusively over the established pairwise X25519 + XSalsa20-Poly1305 channel. The blind-forwarder server sees only opaque ciphertext — it never touches ratchet material.
Message headers carry precise chain_index + sender_token, allowing any receiver to instantly fast-forward their local ratchet if messages were missed during room switches, network partitions, or client migrations. Resilience without sacrificing security.

Migration safety – built for high-tempo, zero-downtime operations
