# Home@ix configurators: data model

`schema.json` records, as read on 24 October 2026:

1. **The prompted (launch) configurator** at
   `home-at-ix-configurator-front.up.railway.app`: a Nuxt 3 front end over a Strapi v5 back
   end (`home-at-ix-configurator-back.up.railway.app`), media on Cloudinary, and the
   Sketchfab Viewer API for the 3D model. The project `home-ix-ever-after-cottage` carries
   eight groups and thirteen controls; each option names the Sketchfab geometry node it
   shows, the material presets it assigns, and its price and carbon deltas. Nested
   controls (Facade Composition under House Type; Brick Color under Brick Bond) appear
   only when their parent option is selected. Displayed price = base 249,999 + the selected
   options' deltas; carbon likewise from base 41 tCO2e.
2. **The natural-language configurator** (`home-at-ix-img-gen.vercel.app`, "House
   Preview"): a single-page app with Clerk sign-in and a Convex back end; the image
   generator is called server-side. The Strapi project's `img_gen_styles` hold the regional
   style prompts (Devon, Herefordshire, Gloucestershire, Norfolk variants) the two apps
   share.
3. **The April 2026 data room's** description of the configurator (Creatomus, Node /
   Strapi / Postgres; WS4) and of the database hosting (Hey Joe, ChromaDB, Ollama,
   ix-anchor-01, Rochen VMs).

The schema is what the prototype configurator and the plans-library index join on: a
design chosen from the Ideas Book list maps to a job in `../potton-library/index.json`,
and the option deltas here price the configuration on top of the turnkey rate.

No credentials were used; everything here is served publicly by the two apps.
