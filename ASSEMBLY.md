# Assembling the splitish

## Parts List
| Item                | Quantity | Price          | Where to Buy                                                                                 | Notes                                            |
|---------------------|----------|----------------|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| splitish PCB        |     1    |   ~$25/5 PCBs  | JLCPCB (or your preferred PCB fab)                                                           |                                                  |
| Kailh Choc Switches |    48    | $6/10 switches | [Novelkeys](https://novelkeys.xyz/collections/switches/products/kailh-low-profile-switches)  |                                                  |
| Kailh Choc Keycaps  |    48    |       ???      | ???                                                                                          | NK used to carry them, idk where to get them now |
| Pro Micro           |     1    |      $7.99     | [SpaceCat](https://spacecat.design/collections/do-it-yourself/products/pro-micro-board)      | Elite-C should also work, if you wanna spend $$$ |
| SMD Reset Switch    |     1    |      $0.69     | [SpaceCat](https://spacecat.design/collections/do-it-yourself/products/smd-switch-alps)      |                                                  |
| 1N4148W-TP Diodes   |    48    |   $0.17/each   | [Digi-Key](https://www.digikey.com/en/products/detail/micro-commercial-co/1N4148W-TP/717311) |                                                  |
| Rubber Feet         |   Many   | Depends        | [Amazon](https://www.amazon.com/322Pcs-Cabinet-Bumpers-Adhesive-Dampening/dp/B07BHP4NGY)     | I'm sure there are plenty of other alternatives  |

## Step 1
Carefully solder all 48 SMD diodes to the bottom of the PCB. On both versions of the splitish PCB, the Cathode end of the diode (the end with the little line) should be facing the user when the keyboard is being used.

![diode alignment](https://raw.githubusercontent.com/RSchneyer/splitish/master/media/diode_alignment.png)

# Step 2
Now that all 48 diodes are properly soldered, you can solder in all 48 switches. The switches should have PCB mount legs that will help align the switch and keep it in place while you solder the metal pins, but a piece of tape can also be used to hold a switch in place.

# Step 3
After soldering all the switches, the next step is to solder the reset button and the Pro Micro. Solder the header pin strips to the PCB first, then the Pro Micro on top, aligned so that all the onboard components face the splitish PCB.

![pro micro and diode](https://raw.githubusercontent.com/RSchneyer/splitish/master/media/reset_and_pro_micro_soldered.jpg)

# Step 4
Attach the rubber bumpons/feet to the underside of the PCB, so that all the solder joints are not touching the work surface. Attach the keycaps, and using QMK, flash the default firmware to the splitish. Assuming you have a QMK environment properly setup on your PC, the command should be

`qmk compile -kb splitish -km default`

Assuming the keyboard now works, you're done with assembly! Wasn't that easy?
