# Bilateral Studio

A static, responsive bilateral stimulation companion for clinician-guided in-person and telehealth sessions. It can be hosted directly on GitHub Pages.

Visual controls include horizontal and bidirectional diagonal movement paths, smooth return-to-origin when a set pauses or ends, target shape, size presets and fine adjustment, color, glow, vertical position, travel width, guide line, side cues, motion trail, and several client-screen backgrounds. Clinicians can also adjust speed, stereo sound, volume, and set duration in real time.

The root `index.html` is the English version. `zh/index.html` is the Chinese version and contains both Simplified and Traditional Chinese with an in-page script toggle. Both versions include a persistent light/dark appearance toggle.

Client links now pause at a **Join & enable sound** step. That required user tap unlocks the browser audio context before the remote session begins. If audio is still blocked, the client can use the persistent **Enable sound** control on the session screen.

Use **Test left–right sound** before a session while wearing stereo headphones. You should hear one tone fully in the left channel, followed by one fully in the right channel.

## Publish on GitHub Pages

1. Create a GitHub repository and upload `index.html` to its root.
2. Open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select `main` and `/ (root)`, then save.

GitHub will provide the public URL after deployment.

## Remote pairing

The page uses PeerJS/WebRTC for ephemeral browser-to-browser control signals. There is no account system or database. The included public signaling service is convenient for initial deployment, but it does not provide a healthcare-specific service agreement or uptime guarantee. Before clinical production use, perform a privacy/security review and consider operating a dedicated PeerServer or replacing the signaling layer with an approved service.

Do not put names, diagnoses, or identifying information in room codes. Video is intentionally not built in; use your organization's approved telehealth platform alongside this page.

## Clinical scope

This software is a stimulus delivery aid—not therapy, a medical device, diagnosis, crisis support, or a substitute for training. It should be used only by appropriately trained clinicians within an established treatment plan.
