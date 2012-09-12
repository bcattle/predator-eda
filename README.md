# Predator EDA
Because you can’t spell EDA without Predator

## Goals

This project is designed to fix everything that sucks about current EDA packages. 

## Design philosophy

Predator EDA is designed to be a tool for professionals. It is designed for the practicing engineer who needs to ship boards. It is designed to 
Preference here is given to people who work in solo/small shops without in-house component libraries and the like.

## Components

### Schematic editor
Minimum feature set needed by professionals to get designs in for manufacture
Use http://raphaeljs.com/ 

### Netlist generation
Basic net rule checking (GND – GND, power-power, etc.)

### Hierarchical block system
Net name scoping

### Part datasheet import
Able to generate a schematic symbol and PCB footprint for a part by just pasting the URL of the datasheet
- Guess pages of footprint, of schematic diagram
- Easy ordering/grouping of schematic pins
- Show side-by-side with pdf for comparison

Understands all major manufacturers’ datasheet styles

### Online parts database
Parts are stored in open format online, and it is easy to use parts from other users. It is also easy to verify whether a part footprint is correct, by side-by-side comparison with the datasheet pdf.

### BOM management
Simple tools to generate bills of materials for lots of one-many boards. Is able to set component purchase overages based on class of footprint (rules like “buy a minimum of 100 0402 package, buy 2 extra SOIC, etc.)
Lightweight integration with distributor APIs shows what parts are in stock, estimated price, and one click to order. 

### PCB editor
Simple, minimalist editor allows basic layout of multilayer boards 
Parametric spacing rules, rule enforcement (e.g. trace-trace, trace-via, etc.)
Has sensible defaults (spacing, # layers) for major manufacturing houses
Can pour copper templates, can specify pouring order 

### Gerber/CAD generation
Able to export standards-compliant Gerber files. Can also export to a 2D CAD format importable by major mechanical CAD programs (DXF, IGES?)

### Support file export
Generates drill files, XYRS for pick-and-place 
Generate PDF assembly diagram?
Can export images

### Versioning
Automatic, like google docs. Easy to diff even complex designs. 

### Lightweight design annotation and review
One click to component datasheet
Share design to others, they can make comments 

## FAQ
### Why not a desktop applicaion?
Why not? An EDA program doesn’t depend on any complicated UI or 3D graphics. Even if it [did](http://en.wikipedia.org/wiki/WebGL), the web technologies get [better](http://www.chromeexperiments.com/globe) every day. Platform and location-independence are nice. 

### Is it free?
Aren’t we getting ahead of ourselves? It isn’t built yet. Perhaps the Github model, where open designs are free but proprietary ones pay a token amount? TBD. Would love to hear your thoughts.  

### Will it import my OrCAD/Eagle/Altium files?
No. A pluggable import plugin infrastructure could be added later. 

### Does it do simulation?
No. Use [Paul Falstad’s circuit simulator](http://www.falstad.com/circuit/) or [LT Spice](http://www.linear.com/designtools/software/). 
Practicing engineers spend 
If you need specialized features like … then you need a specialized CAD package. 

### Can I get involved
Definitely. This is potentially a complicated undertaking. Please drop me a line if you have an opinion about something. 
