## Confirm it is working

Initially, Plover is set up to use your computer keyboard as a steno machine. If you have a professional stenography  machine or the Stenomod, you'll need to configure Plover to look for your machine.

### Keyboard

By default, Plover will use your keyboard as its input device. 

1. Run Plover.
1. Click the Output: **Enable** radio button. 
 
You may like to go into Plover's `Configure > Display` settings and turn on either the stroke display or the suggestions window.

#### Write "Hello World"

To confirm Plover is working correctly, you may try to write "Hello, world." into a text editor with Plover, using a QWERTY keyboard:

1. Run Plover. 
1. Click the **Enable** radio button.
1. Open a text editor.
1. Simultaneously press `R`, `N`, and `O` (left index finger on `R`, right thumb on `N`, and right ring finger on `O`), and then lift your fingers off the keys. <br>The word `Hell` appears.
1. Simultaneously press `R`, `F`, and `V` (left index finger between 'R' and 'F', and left thumb on 'V'), and then lift your fingers off the keys. <br>The `o` appears. 
1. Simultaneously press `J`, `K`, `L`, and `;` (right index finger on `J`, right middle finger on `K`, right ring finger on `L`, and right little (pinky) finger on `;`), and then lift your fingers off the keys. <br>The comma appears.
1. Simultaneously press `D`, `V`, `J`, `O`, and `[` (left middle finger on `D`, left thumb on `V`, right index finger on `J`, right ring finger on `O`, and right little (pinky) finger on `[`), and then lift your fingers off the keys. <br>`world` appears.
1. Simultaneously press `U`, `I`, `O`, and `P` (right index finger on `U`, right middle finger on `I`, right ring finger on `O`, right little (pinky) finger on `P`), and then lift your fingers off the keys. <br>A period appears.

If you see different output, you might check that you're using the right protocol for your [stenography machine](https://github.com/openstenoproject/plover/wiki/Beginner's-Guide:-Get-Started-with-Plover#stenography-machine).

#### Practice sentences

You can practice sentences that (mostly) only need two keys at once, on the [StenoJig](https://joshuagrams.github.io/steno-jig/two-key) website.

#### Use the correct body posture and finger placement

Your fingers should be curled slightly, so you press the keys using the tips of your fingers. 

<img src="http://stenoknight.com/plover/stenqwerty.png" width="450">

On a QWERTY keyboard, you move your hands half an inch up so that your left thumb is resting on the cracks between the `C` and `V` keys and your right thumb is resting between the `N` and `M` keys. The rest should fall into place. 

| QWERTY layout|Maps to steno layout |  
|:---:|:---:|
|`QWER   TY   UIOP[`|`STPH  **   FPLTD`|
|`ASDF   GH   JKL;`|`SKWR   **   RBGSZ`|
|`CV   NM`|`AO   EU`| 

See also:

* [Basic Hand Posture on the Steno Machine](https://www.youtube.com/watch?v=YfHNPW6EnHo)
* [Basic Body Position for Steno Students and Pros](https://www.youtube.com/watch?v=s_zyxgQvNEU)

### Stenography machine

Plover supports several protocols that are in use by various professional stenography machines. To configure Plover to the protocol your machine uses:

1. Run Plover and click the **Enable** radio button.
1. Click the **Configure** button on the Plover Dialog screen. The Plover configuration screen appears. 
1. On the **Machine** tab, select the protocol your machine uses. 
1. Click **Save**.

See [Supported protocols](https://github.com/openstenoproject/plover/wiki/Supported-Hardware#supported-protocols) for more information.