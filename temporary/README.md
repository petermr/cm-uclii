# cm-uclii
## temporary
A directory of temporary outputs from problem cases in initial parsing. The primary intent is for downstream software to consume these and report success or feed back modifications.

### unrotated
These tables were originally rotated anticlockwise by 90 deg (+90 in current coodinates) in the paper (turn head left to read). The code snippet has been appllied:

```
Real2 centre = bbox.getSquareBoxCentre(BoxDirection.LEFT);
			g.appendChild(new SVGCircle(centre, 3.0));
			Angle clock90 = new Angle(-Math.PI/2.);
			Transform2 t90 = new Transform2(clock90);
			for (SVGText text : textLists) {
				SVGText text1 = new SVGText(text);
				text1.rotateTextAboutPoint(centre, t90);
				g.appendChild(text1);
			}
```

which rotates the page about the "square centre" of the table clockwise 90 deg (-90 ).

The results have been written out and presented here.

### colorpanel
These are pages with one or more "colorpanel"s - areas of the page filled with a single colour. In practice these are someties made of several butting panels without visible dividing lines. The Panels are converted to `SVGRect`s and written out

### ruled
These are tables with horizontal rules which do not firs the mainstream patterns of T<r>H<r>B<r>F , generally having many rules in the body.

### split
These are tables split into 2 or more compoenents (not currently included).
