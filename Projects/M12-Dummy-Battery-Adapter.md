\---

type: project

name: 3D Print and Wire M12 Dummy Battery Adapter for 12V PSU or Car Battery

status: planned

priority: medium

target-item: \[\[Cordless-Screwdriver]]

location: \[\[Screw-Bucket]]

estimated-cost: 45

due: \[YYYY-MM-DD]

\---



\# M12 Dummy Battery Power Adapter Project



\*\*Goal\*\*: Print a dummy M12 battery shell that plugs into the \[\[Cordless-Screwdriver]] (or any M12 tool) and runs off a 12V bench power supply or car battery — perfect for long bench sessions without killing real batteries.



\*\*Researched Specs\*\* (for 2401-20 screwdriver)

\- Voltage: 12V nominal

\- Peak current draw: 12–18 A under heavy load/stall (Milwaukee does not publish official numbers; tool has electronic protection). \*\*Design/sizing for 20 A conservative\*\* to cover inrush and safety margin.

\- Wire (10 ft one-way): \*\*12 AWG copper\*\* (round-trip 20 ft). Voltage drop at 20 A ≈ 0.35 V (<3% of 12 V) — perfect. Use 10 AWG if you want near-zero drop or plan bigger M12 tools.

\- Power supply: 12 V DC regulated \*\*≥25 A\*\* (e.g., Mean Well LRS-350-12 or similar). Car battery works with 30 A inline fuse.

\- Pinout (M12 interface): Large outer contacts = + (positive) and – (negative). Thermistor pin (T) needs a \*\*10 kΩ resistor\*\* to – (common trick to fool the tool). Ignore the two small data pins for a simple dummy.



\*\*Recommended 3D Models\*\* (free STL – print in PETG/ABS)

\- Best ready-to-wire dummy: https://makerworld.com/en/models/1308040-milwaukee-m12-dummy-battery-ac-adapter (remix of CuriousTech – clean holes for wires)

\- Alternative with switch/fuse cutouts: https://www.thingiverse.com/thing:7253208

\- Exact interface reference (for measurements if you want to modify): https://grabcad.com/library/milwaukee-m12-drill-battery-1



\*\*Example printed dummy (white shell with wire exiting)\*\*  



<grok-card data-id="425729" data-type="image\_card" data-plain-type="render\_searched\_image"  data-arg-image\_id="0AGnR"  data-arg-size="LARGE" ></grok-card>





\*\*Parts List\*\*

\- 12 AWG red + black wire (\~11 ft)

\- 30 A automotive inline fuse holder + fuse

\- SPST toggle switch (rated 20 A+)

\- 10 kΩ ¼ W resistor

\- Heat-shrink tubing + solder or crimp connectors

\- Optional: XT60 or banana plug pair for quick PSU disconnect

\- Filament for printing



\*\*Safety Notes\*\*

\- Add the 30 A fuse close to the power source.

\- Use proper strain relief where wire exits the print.

\- Test at low voltage first.

\- Do not exceed 20 A continuous (tool will shut down anyway).



\*\*Tasks\*\* (check off with Tasks plugin)

\- \[ ] Download \& print dummy shell (0.2 mm layer, 3–4 walls)

\- \[ ] Drill wire exit hole if needed

\- \[ ] Solder 12 AWG wires to +/– terminals + 10 kΩ resistor to T

\- \[ ] Install fuse holder and switch in line

\- \[ ] Connect to 12 V 25 A PSU or car battery

\- \[ ] Test with \[\[Cordless-Screwdriver]] at low speed

\- \[ ] Label and store in \[\[Screw-Bucket]]

\- \[ ] Update project status to "complete" + add photos to this note

