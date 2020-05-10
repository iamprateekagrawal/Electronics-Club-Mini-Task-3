### Finger Ring
This project involves ideation for a ring that glows when wore in any finger.

**Intial design:** basically involves a butoon switch inside the ring which gets pressed when wore and glows the light on ring. However, button presses back and hurts the fingers, so we need a better innovative design.

**Constraints:**
* Size shouldnt exceed much.
* Power is limited as one/two button cells seems only possibility.
* Comfortability shouldnt be compromised.
* Should be made from commercially available components.

**Ideation:**

Available methods | What's accomplished by this method | Drawbacks of this design
------------------|---------------------|-------------------------
**[1]** LED+LDR -> Another small LED directing rays to LDR all inside the ring - this link breaks when ring is wore and activates the circuit | Meets requirements and eliminates any other possibility of glowing ring other than when wearing it | Consumes more power and not that compact
**[2]** Touch sensor -> Replacing the button switch with a 'touch key module' which activates circuit when touched (which is when wore) | Simple, cheap, compact and comfortable with all constraints satisfied | May light up with dust accumulation or casual touch/movement

The *second design* looks more simple and feasible presently. We shall go with it!

**Feasibility check:**
* [TTP223](https://pdf1.alldatasheet.com/datasheet-pdf/view/1179637/TTELEC/TTP223.html) capacitive touch key can be used as a touch sensing module.
* Two button cells (each avg 1.5V output) can work as TTP223 requires 2-5V power input.
* Overall cost is also less as controller costs around Rs.50 and rest LED & wires - all components at max Rs.100 including shipping charges(if any)
* All these things, along with an LED (which pops outside), can be sized inside a finger ring in a compact manner with wires soldered to the respective components. Being specific - TTP223 is around 1cmX1cm, cells of ~1cm dia, rest wiring connections.

![TTP223](https://rarecomponents.com/store/image/cache/data/0-1921-1-400x400.jpg)

**Final conclusion:** A simple design is ideated to glow LED when touch sensor activated while wearing the ring, keeping in mind about constraints like size, cost, power and comfotability.
