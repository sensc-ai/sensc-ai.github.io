# SENSC approval page

A static page that lets Tid approve a runner request with his phone passkey (Face ID).

* `#setup` creates the passkey and writes the message Tid pastes into the runner chat.
* `#r=<payload>` shows one approval request and signs it with the passkey.

The page stores nothing on a server and sends nothing anywhere. The payload rides in the URL fragment, which browsers do not send to the server. The runner verifies each approval itself with the `sensc_approval` kit, against the passkey it pinned from Tid's own message.
