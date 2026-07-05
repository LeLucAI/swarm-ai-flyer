# img2img prompts — Anduril placeholders → Swarm.ai style

**Workflow:** open the source URL, pause the video at a nice frame, screenshot it (or download the mp4 and grab a frame), then use that frame as the input image for OpenAI image editing (gpt-image-1, "edit" / img2img mode) with the prompt below. Keep `fidelity` low-to-medium so composition survives but style transforms.

**Global style block — append to every prompt:**

> Swarm.ai brand style: pure black background (#050505), wireframe/particle graphics in amber (#F5A700) and teal (#00A5AB), sparse red (#E5484D) accents only for tracked threats, thin technical linework, subtle glow, dark military-tech aesthetic, high contrast, cinematic, no text, no logos, no watermarks.

---

## 1. Particle torus (card 02 — "Sees day + night")
**Source:** https://cdn.sanity.io/files/61nocsj5/production/03461aaa37e529c90a1ca19ac16482d710ae8527.mp4

> Transform this monochrome particle torus into a hemispherical dome of surveillance coverage seen in slight perspective: a dome made of fine amber particle rings over a faint teal wireframe ground plane, with a small glowing sensor node at the center emitting the dome. A few tiny amber triangle contacts on the dome surface, one boxed by a thin dashed red square. Keep the dark void background and the particle-cloud texture of the original. + [global style block]

## 2. Data tunnel (card 03 — "Thinks on the edge")
**Source:** https://cdn.sanity.io/files/61nocsj5/production/21c80f13e2efb35d9a3ff86db145c01ca68812b0.mp4

> Transform this monochrome particle data-tunnel into a stream of compact 3D track data: sparse glowing amber dots and short teal dash-segments flowing from left (dense, chaotic point cloud of raw imagery) through a narrow bright aperture into a thin, ordered single line of amber packets on the right — visualizing "gigabytes of video in, kilobits of 3D tracks out". Keep the perspective convergence and particle texture of the original. + [global style block]

## 3. Particle disc (card 04 — "Small & deployable")
**Source:** https://cdn.sanity.io/files/61nocsj5/production/cc303b7dfedf19f364ba5c0ec97df3de4e75ec11.mp4

> Transform this monochrome particle disc into a top-down radar-style coverage map: concentric faint teal range rings on black, a rotating amber sweep wedge, four small teal-ringed sensor nodes arranged across the disc connected by thin dashed teal mesh lines, tiny amber triangle contacts at the edge. Keep the elliptical perspective and particle grain of the original. + [global style block]

## 4. Mission-cycle animation (hero / section background)
**Source:** https://cdn.sanity.io/files/61nocsj5/production/a4edc751d8d8c7c961e615e5b78e7330fe854b6b.mp4

> Transform this dark UI animation frame into a wide cinematic 3D battlespace reconstruction: perspective teal wireframe terrain with rolling hills on black, a grey flying-wing stealth drone above it enclosed in a thin dashed red 3D bounding box with a dotted amber trajectory line behind it, three small sensor nodes on the terrain linked by dashed teal lines, faint amber tracking rays from nodes to the drone. + [global style block]

## 4b. Wingsuit → drone (video-to-video, our own footage)
**Input:** `assets/recon-world.mp4` (our 3D reconstruction with wingsuit pose trail)

> Video-to-video (Runway Gen-3 / Sora style transfer, low strength): keep the 3D-reconstructed terrain, camera path and the trail of tracked poses exactly as they are, but replace every wingsuit flyer instance with a small grey flying-wing UAV (stealth delta shape, no propellers visible). Preserve the photogrammetry texture look of the terrain and the white void background. No text, no logos.

## 5. Bonus — our own city hero (no Anduril source)
**Input:** `assets/city.png` (our aerial night-city shot with red detection boxes)

> Enhance this real aerial night photograph of a city: deepen blacks toward #050505, shift the sodium street-light glow slightly toward amber #F5A700, add a very subtle teal wireframe terrain-mesh overlay hugging the cityscape in the lower third, and sharpen the existing thin red detection rectangles. Keep it photographic and realistic — augmented-reality overlay look, not an illustration. No text, no logos.

---

**After generating:** drop results into `assets/` as `gen-dome.png`, `gen-tunnel.png`, `gen-disc.png`, `gen-battlespace.png`, `gen-city.png` and swap the `<video>`/`<img>` sources in `index.html` (search for "PLACEHOLDER"). The Anduril hotlinks must be gone before this page or its print goes to anyone external.
