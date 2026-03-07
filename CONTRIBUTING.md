# Contributing

Contributions to Pinhead are **open**. We'd love for you to be involved! If you'd like to add or improve some icons, by all means open an [issue](https://github.com/waysidemapping/pinhead/issues/new) or [pull request](https://github.com/waysidemapping/pinhead/pulls/new). See the [open issues](https://github.com/waysidemapping/pinhead/issues) to browse icons that folks have requested.

By contributing, you agree to license your original work as [CC0](/LICENSE) and to upload license-compatible material only.

## Contributor FAQ 

#### Is my icon in scope?

Probably! While this project is focused on maps, you'd be surprised how many icons that don't seem geographic at all end up making useful pinheads.

#### Why 15x15 pixels?

The 15x15 rule mostly comes from Temaki, which inherited it from Maki. Compared to OSM Carto's 14x14, it's pretty handy to use an odd number so that a 1px wide line can be perfectly centered. Going down to 13x13 is feasible for the some icons but starts to get hairy when trying to depcit more complex things. Maki actually used to distribute 11x11 versions of icons (sooo tiny!) but [dropped them](https://github.com/mapbox/maki/commit/96e8b4c5941d687ddf0fde527ad54dde5559eef2) in v7. Probably the benefit didn't justify the maintence overhead in the age of high-DPI displays. So yeah, 15x15 just feels like the sweet spot.

#### I found a cool icon online. Can I upload it?

Maybe! Any external icons **must** have a compatible license (CC0 or equivalent). If you're unsure, just ask. It's not okay to upload someone else's work if they retain copyright or have assigned usage restrictions.

## Design guidelines

If the following sections seem too technical or intimidating, feel free to just ignore them and go straight to opening a PR for your cool icon. These are intended only for managing internal consistency and I'd be happy to give you pointers after the fact. There aren't many hard rules here. Have fun with it!

#### Visual design

* Legibility
  * Icons should be basically legible when displayed at 15x15 screen points on a 2x pixel density display.
  * _Ideally_ icons should also be legible on a traditional 1x display at 15x15 pixels, but alas this is not always possible for some of the more complex graphics.
  * Snapping shapes to 1px and 0.5px increments on the 15x15 pixel grid can often help.
  * Shapes that are too small, overly detailed, or too close together usually look muddy at small sizes.
  * Screen legiblity is more of an art than a science, try experimenting.
* Perspective
  * Most things are more iconic from one angle than another. Prefer in this order:
    * <img src="https://pinhead.ink/v1/car.svg" height="15px" width="15px"/> A straight-on horizontal perspective
    * <img src="https://pinhead.ink/v1/bicycle.svg" height="15px" width="15px"/> A horizontal side profile
    * <img src="https://pinhead.ink/v1/railway_track.svg" height="15px" width="15px"/> A top-down vertical perspective
    * <img src="https://pinhead.ink/v1/sandbox_with_sand_trowel.svg" height="15px" width="15px"/> 3D (sparingly!)
  * Multiple icons for different perspectives of the same thing can be okay if they're all iconic.
* Orientation
  * People, animals, vehicles, etc. depicted in profile should be facing to the right.
    * Except when moving backwards (e.g. boats on slipways).
    * Except when standing in opposition to movement (e.g. the "stop arm" checkpoint officers).
  * Hand tools should be pointed to the right.
  * Icons with major and minor elements positioned side-by-side should have the major element on the left and minor element on the right.
  * Multiple icons for different orientations generally isn't useful. Users can manually rotate or flip icons if desired.
    * Except when a different orientation gives the icon a different meaning (e.g. arrows).

#### SVGs

* SVGs must contain only shapes that can be rendered with `fill`. Rendering with `stroke` is not supported.
* SVGs must have viewBox="0 0 15 15" with no elements extending outside this frame.
* The build scripts will take care of most other SVG formatting issues.

#### Filenames

* The filename is the only icon ID, which means changing a filename after publishing will break stuff and should be avoided.
* Filenames should be literal and descriptive at the risk of being verbose.
  * E.g. prefer <img src="https://pinhead.ink/v1/giraffe.svg" height="15px" width="15px"/> `giraffe` to `zoo` and <img src="https://pinhead.ink/v1/greek_cross.svg" height="15px" width="15px"/> `greek_cross` to `medicine`.
* Two files should have similar names if the components of their icons are similar.
* Two files cannot share a name, even if they are in different subdirectories.

#### Subdirectories
* The subdirectory of an icon is used only for developer-side convenience and has no effect on distributed icons.
* Files are broadly organized by design, not by content.
* Some subdirectories contain README.md files which give more detailed information.

## AI/ML policy

Icons generated by AI/ML models are assumed to be protected by copyright unless the model owner releases the rights to said icons AND said models have been trained exclusively on public domain sources or sources owned by the model owner. As this is generally never the case, and since major AI/ML model owners are known to be disingenuous about this stuff to the detriment of artists, AI-generated icons will not be considered for inclusion in Pinhead at this time.

Since this repository is licensed in the public domain, you are technically free to train AI/ML models on the icons. But come on, wouldn't you rather draw a <img src="https://pinhead.ink/v1/bison.svg" height="15px" width="15px"/> lil guy and feel a little joy for once?

## Code of conduct

You will be banned if you engage in harassment, unprofessional conduct, or copyright infringement. Be nice or be elsewhere :)