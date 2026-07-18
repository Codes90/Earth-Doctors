# Your Photos Go Here

Drop your photos into this folder using these exact filenames and they appear
on the site automatically (until then, the site shows its built-in colors):

| Filename             | Where it appears                       |
|----------------------|----------------------------------------|
| `hero-home.jpg`      | Home page — big top banner             |
| `hero-philosophy.jpg`| Philosophy page banner                 |
| `hero-atelier.jpg`   | Atelier (shop) page banner             |
| `hero-retreats.jpg`  | Retreats page banner                   |
| `hero-bookings.jpg`  | Bookings page banner                   |
| `hero-education.jpg` | Education page banner                  |
| `hero-journal.jpg`   | Journal page banner                    |
| `hero-contact.jpg`   | Contact page banner                    |
| `founder.jpg`        | About section portrait on the home page |

Recommended: wide landscape photos, at least 1920px across, JPG format.
Product photos go in the `products/` subfolder — see the README there.

Bonus after adding `hero-home.jpg`: in `public/index.html`, update the
`og:image` meta tag (near the top) to
`https://earth-doctors.com/images/hero-home.jpg` so social-media link
previews use your photo, and optionally delete the Unsplash fallback line in
the `#heroImage` style block.
