### Finger Ring
This project involves ideation for a ring that glows when wore.

**Intial design:** basically involves a butoon switch inside which gets pressed when wore and glows the light on ring. However, button presses back and hurts the fingers, so we need a better design.

**Constraints:**
* Size shouldnt exceed much.
* Power is limited as button cells seems only possibility.
* Comfortability shouldnt be compromised.
* Should be made from commercially available components.

**Ideation:**

Available designs | What's accomplished | Drawbacks of this design
------------------|---------------------|-------------------------
**[1]** Another small LED directing rays to LDR all inside the ring - this link breaks when ring is wore and activates the circuit | Meets requirements and eliminates any other possibility of glowing ring other than when wearing it | Consumes more power and not that compact
**[2]** Replacing the button switch with a 'touch key module' which activates circuit when touched (which is when wore) | Simple, cheap, compact and comfortable with all constraints satisfied | May light up with dust accumulation or casual touch/movement

The *second design* looks more simple and feasible presently. We shall go with it!

**Feasibility check:**
* [TTP223](https://pdf1.alldatasheet.com/datasheet-pdf/view/1179637/TTELEC/TTP223.html) can be used as a touch sensing module.
* Two button cells (each avg 1.5V output) can work as TTP223 requires 2-5V power input.
* All these things, along with an LED, can be sized inside a finger ring in a compact manner with wired soldered to the respective components.

**Final conclusion:** A simple design is ideated to glow LED when touch sensor activated while wearing the ring.
