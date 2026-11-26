# Benstore

On-device iOS sideloader (Apple ID signing) + Benstore Installer for Mac.

- **Mac installer:** [Benstore-Installer.zip](https://benjaminsoble91-eng.github.io/benstore/Benstore-Installer.zip)
- **iPhone app:** [Benstore.ipa](https://benjaminsoble91-eng.github.io/benstore/Benstore.ipa)

Both apps check `update.json` here and update themselves with one tap.

**Downgrade:** [all past versions](https://benjaminsoble91-eng.github.io/benstore/versions.html). Open the page in Safari, tap Get, then Share → Benstore. `update.json` → `versions` lists every build with its checksum.

## Remote install (admin panel)

Open **[admin.html](https://benjaminsoble91-eng.github.io/benstore/admin.html)** and load your `benstore-admin-key.json` (kept in that browser only, never uploaded). Any iPhone that has opened Benstore shows up in the panel; pick one, give an IPA URL, and send. The phone checks the request is signed by your key, then asks its owner three times before installing. Owners can turn those prompts off in **Settings -> Remote installs -> Allow remote downloads** (off by default). Remote install itself is always on. Requests expire after 10 minutes and can't be replayed or spoofed.
