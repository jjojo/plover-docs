## Keyboards

If you don't have a steno machine, you can use a keyboard that supports N-Key Rollover (NKRO).

<img src="http://www.zalman.com/DataFile/product/B_0001_%EB%A0%88%EC%9D%B4%EC%96%B4%204.jpg" width="300"/>

### What's NKRO?

This is a feature of some keyboards that means that you can press as many keys as you want simultaniously, and they will all register. Typical keyboards stop working correctly when you press somewhere between 4 and 7 keys at once.
For more information, see the [Wikipedia entry about NKRO](http://en.wikipedia.org/wiki/Rollover_(key)#n-key_rollover).

### How do I know if my keyboard has NKRO

In general, most keyboards will not be NKRO. "Gamer" and mechanical keyboards are most likely to have NKRO, while budget as well as laptop keyboards are unlikely to have NKRO.

#### Test #1: Double Shift

**Note: this test results in a false positive on some Macbooks**

To test your keyboard for NKRO capability:

1. Open up a text editor.
2. Hold down both shift keys.
3. Type each letter on your keyboard (from A-Z).

> **Note**: You must hold down both shift keys while you type each letter on your keyboard.

If all keys are typed into the text editor, your keyboard probably has NKRO.

#### Test #2: Keyboard Ghosting Test

The [in-browser steno demo](http://www.openstenoproject.org/demo/) provides a browser-based application that lets you test your keyboard's capabilities for registering multiple key presses with simulated steno output.

To test your keyboard:

1. Open your web browser and go to the [in-browser steno demo](http://www.openstenoproject.org/demo/).
1. Click in the **Output box** to start
    * Each key you press will light up in the picture of a keyboard. 
1. Press the middle row keys `asdfjkl;` **all at once**.
    * With a normal keyboard only 6 of the 8 keys will light up (likely fewer).
    * If your keyboard has N-key rollover, all 8 keys will light up. 
1. Press other multiple-key combinations, such as `yuhj`, and see if they all light up. Ideally, your keyboard should register the entire first two rows of your keyboard at once, plus `c`, `v`, `b`, and ` n`.

### What if my keyboard is not capable of NKRO?

If you don't have a keyboard that's capable of NKRO, but still want to give Plover a try, you can arpeggiate/roll the keyboard chords. More info can be found at the bottom of [this post](http://plover.stenoknight.com/2011/02/plover-211-released.html).

### Known supported keyboards

> **Warning**: Be wary of false advertising; some keyboards are advertised as NKRO or anti-ghosting, but are limited to certain combinations. Check reviews to get confirmation before making a purchase. Some keyboards might only support full-NKRO over a PS/2 connector (the [old-style plug](https://en.wikipedia.org/wiki/PS/2_port#/media/File:Ps-2-ports.jpg).) Full NKRO over USB is possible. Many keyboards do it well, and will work with Plover.

The following machines have been confirmed by users to work with Plover after actually trying it:

| Product Name                | Manufacturer           | Comments        | Price
| --------------------------- | ---------------------- | --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------
| Anne Pro II | Obinslabs | NKRO over USB; 6KRO over bluetooth; Works on Mac | $20-100
| Aukey KM-G9 | Aukey | NKRO over USB | $35-50
| I-500 Victop (compact: 87 keys)     | Eastern times tech | NKRO over USB   | [27 GBP](https://www.amazon.co.uk/Water-Resistant-VicTop-Mechanical-Waterproof-Anti-ghosting/dp/B01DBYNVSY/)
| DareU DK87 (red switch) | DareU | NKRO over USB (Tested on Linux), however some keys may be stuck after released. Discontinued model. There is a [similar model](http://www.dareu.com/?m=home&c=View&a=index&aid=169), they may have the glitch mentioned above or not. | < $30
| TOMOKO (87 key Mechanical Keyboard) | TOMOKO               | NKRO over USB (Works on Mac)   | [$30](https://www.amazon.com/TOMOKO-Water-Resistant-Mechanical-Keyboard-Non-Conflicting/dp/B01DBJTZU2/)
| K552 | Redragon | NKRO over USB | [$35](https://www.amazon.com/Redragon-KUMARA-Backlit-Mechanical-Keyboard/dp/B016MAK38U)
| X51 (Gaming Mechanical Keyboard 87/104) | Metoo                | NKRO over USB   | [$40](https://www.aliexpress.com/item/Metoo-Gaming-Mechanical-Keyboard-87-104-Anti-ghosting-Luminous-Blue-Red-Black-Switch-Backlit-LED-wired/32782819448.html) 
| ZM-K600S                    | Zalman                 | NKRO over USB   | [$40](http://www.amazon.com/Zalman-Unlimited-Multi-Key-keyboard-ZM-K600S/dp/B0196J3IPE)
| K66                         | Corsair                | NKRO over USB   | [$55](https://www.amazon.com/CORSAIR-K66-Mechanical-Gaming-Keyboard/dp/B072LTTNVS/)
| K63                         | Corsair                | NKRO over USB (Works on Mac!) | [$80](https://www.amazon.com/Corsair-CH-9115020-NACORSAIR-Compact-Mechanical-Keyboard/dp/B06XC1WNPT)
| K95                         | Corsair                | NKRO over USB   | [~$200](https://www.amazon.com/CORSAIR-PLATINUM-Mechanical-Gaming-Keyboard/dp/B01MU3R9VM)
| STRAFE                      | Corsair                | NKRO over USB   | [$80](https://www.amazon.com/CORSAIR-STRAFE-Mechanical-Gaming-Keyboard/dp/B012B6X7MI/)
| CM Storm Quickfire TK       | Cooler Master          | NKRO over USB (Doesn't work on Mac)   | [$85](http://www.amazon.com/CM-Storm-QuickFire-TK-Mechanical/dp/B00A378L4C/)
| Vengeance K65               | Corsair                | NKRO over USB   | [$90](http://www.corsair.com/en/gaming-peripherals/gaming-keyboards/vengeance-k65-compact-mechanical-gaming-keyboard.html)
| C413 Carbon                  | Logitech             | 26KRO            | [$90](https://www.logitechg.com/en-us/products/gaming-keyboards/g413-mechanical-gaming-keyboard.920-008300.html)
| Francium Pro                  | Deck            | NKRO over USB when in "lightning" mode (Fn + F10). Full NKRO works on Windows and Linux, but is rumored NOT to work on Macs (you'd be stuck with 6KRO).  | [$94](https://mechanicalkeyboards.com/shop/index.php?l=product_detail&p=690)
| Noppoo Choc                 | Noppoo                 | NKRO over USB (works on Mac without adapters)   | [$95](http://www.amazon.com/Noppoo-84-Technology-Mechanical-Keyboard/dp/B0091Q34EI/ref=sr_1_1?s=pc&ie=UTF8&qid=1458020924&sr=1-1-spons&keywords=noppoo+choc+mini&psc=1)
| Apex M750 TKL               | SteelSeries            | NKRO over USB (Works on Mac, but for some reason if you install the SteelSeries Engine it stops working) | [$120](https://www.amazon.com/dp/B076XDTLBB)
| G710+                       | Logitech               | NKRO over USB   | [$130](http://gaming.logitech.com/en-us/product/g710plus-mechanical-gaming-keyboard)
| Majestouch-2                | Filco                  | NKRO over USB   | [$167](http://amzn.to/oLy2xQ)
| Das Keyboard 4 Ultimate     | Das Keyboard           | NKRO over USB requires key sequence to enable. See fine print on underside of keyboard   | [$169](http://shop.daskeyboard.com/products/das-keyboard-4-ultimate/)
| Apex M800                   | SteelSeries            | NKRO over USB   | [$199](https://steelseries.com/gaming-keyboards/apex-m800)
| Ergo Pro                    | Matias                 | NKRO over USB   | [$200](http://matias.ca/ergopro/pc/)
| Ultimate Hacking Keyboard   | Ultimate Gadget Labs   | NKRO over USB   | [$250](https://www.crowdsupply.com/ugl/ultimate-hacking-keyboard)
| Ergodox                     | Ergodox                | NKRO over USB   | [Parts €160.00 - Assembled €247.00](https://falba.tech/customize-your-keyboard/customize-your-ergodox/)
| Ergodox EZ (swappable switches) | ZSA Technology Labs, Inc.| NKRO over USB  | [EZ Only $270 - All Upgrades $354+](https://ergodox-ez.com)
| Planck EZ (swappable switches) | ZSA Technology Labs, Inc. | NKRO over USB  | [ Planck only $180 - W/LED Backlighting $195 ](https://ergodox-ez.com/pages/planck)
| Model01                     | Keyboard.io            | NKRO over USB   | [$329](http://shop.keyboard.io)

#### Which type of key switch should I choose?

Because you hit many keys with steno at once, there are two properties that are useful to have in a mechanical keyboard switch for steno: a **light actuation force** on a **linear** switch.

The light actuation makes it easier on your hands. For a chord like `TKPWHRAOEUGD` (gliding), you are hitting 8 keys with your left hand. That means that whatever switch force you need to depress one key, you have to push 8-times as much. For a 80cN (~80 grams, ~2.9 oz) switch, that's 640cN (~640g, ~22.6 oz). For this reason, your wrists will have a much easier time working with your machine if its actuation force is as light as possible.

The linearity is recommended because it's been found that the tactile feedback that one gets from an individual switch is not as useful when you are receiving 4-10 of those feedbacks at once. The brain just doesn't process all the fingers' feedback in a useful manner. And since the bump usually requires a small addition to the actuation force, we recommend keeping it linear and simple.

Professional steno machines, historically, always bottomed out (meaning the keys are pressed until they can no longer travel; the bottom.) Newer machines use more complicated mechanisms for detecting key travel, often using magnets and the hall effect to determine where the key is, allowing for customizable actuation points. The typical force required for a modern steno machine is between **10cN and 20cN**, with some extremes on either end for personal preference. The travel of a typical lever steno machine is usually between **2mm and 30mm**. The lower end is found in machines like the LightSpeed (nonlever), where the higher end is around the maximum that you can configure a lever machine to stroke.

Most of the mechanical switches have a 2mm actuation point and 4mm travel/bottoming out, but some community members have found that "speed switches" with an earlier actuation point (usually 1.1-1.4mm) are better for steno due to their increased sensitivity.

| Switch | Stat | Note | Machines |
| ------ | ---- | ---- | ------- |
| Gateron Clear / White | 35 cN linear | Best stock option available on the market | Stenomod uses this switch |
| Matias Red | 35 cN linear | Feels heavier than 35 cN switches due to having a "flat" force curve. Matias also has a different stem from Cherry | SOFT/HRUF uses this switch |
| Cherry MX Red | 45 cN linear | | |
| Kailh Silver | 50 cN spring* linear | Has an early actuation (1.1mm vs 2mm) | |
| Cherry MX Brown | 45 cN bumpy | While not ideal compared to other options, this switch is still a better choice than blues, blacks, and other Cherry switches | |
|Kailh Choc Red | 50 cN spring* linear | | The Georgi uses this switch |

\* The Kailh silvers and Choc reds use a spring that would cause a 50 cN actuation point at 2mm, but since they actuate earlier (1.1mm), the force required is nearer to 35 cN.

There are other methods to decrease actuation force for even these switches. This includes:

- Putting the Gateron Clear's 35 cN spring into the Kailh Silver for its earlier actuation point.
- Trimming the springs of a linear switch by several mm to reduce force.
- Using an aftermarket spring with lower forces, such as a prototype 20 cN spring that isn't yet released to the wider market.
- Removing the leaf-spring (not the primary spring) in the Matias Red switch to make the force curve less flat.

### Adapt a keyboard for steno use

![](https://c1.staticflickr.com/5/4202/34180678224_98d3e26f1f_n.jpg)

Most keyboards have the keys in staggered rows, which can make it difficult to press two keys in a column with a single finger. To adapt a keyboard for steno use, you can use:

* Keytoppers
* Keycaps

You can also use a keyboard with an ortholinear layout.

#### Keytoppers

Laser-cut keytoppers are in the shape of the keys on a steno machine. You stick them on top of the relevant keys on the keyboard. You can buy laser-cut keytoppers from the [Plover Store](http://plover.deco-craft.com/). You can also make your own keytoppers out of plastic or even coins.

![Laser-cut keytoppers sitting in a pile](http://i.imgur.com/cjWDy2J.jpg)
 
#### Keycaps

If you have a mechanical keyboard, it is likely your keys have a [Cherry MX stem](https://deskthority.net/wiki/Cherry_MX) and will work with custom keycaps. You can replace the existing keycaps on your keyboard with different keycaps, to improve the layout for stenoing.

- [StenoToppers](https://cemrajc.github.io/stenotoppers/) is a 3D printed keycap set designed by Jason Cemra. It aligns the rows, raises the keys, and reduces the keycap tapering, slant and gap. The 3d model (.stl) files are available on Github. If you have access to a 3D printer, you can download .stl files and print them for a negligible cost. Otherwise, you would need to use a 3D printing service.

  <img src="http://imgur.com/FRwXu8x.jpg" width="400">

- The [G20 keycap set](http://pimpmykeyboard.com/g20-blank-keycap-sets/) from Signature Plastics is a great set for steno, and will fit on an ErgoDox or other mechanical keyboard. The keys have a direction, so for optimal comfort, you should angle the top row of steno (`STPH...`) down, so that they are close to the bottom row (`SKWR...`)
- You can 3D-print a [steno-friendly keycap](https://github.com/morinted/stenomod_case).

Keys that have little space between them are good for steno, because then you can hit two neighboring keys with one finger (which is frequently necessary).

### NKRO keyboards with an ortholinear layout

Keyboards with an "ortholinear" layout have the keys in straight columns. This is handy for steno, as it makes it easier to press two keys in a column with a single finger. 

The following machines have been confirmed by users to work with Plover after actually trying it:

| Product Name                       | Manufacturer       | Protocol/Connection | Comments                |
| ---------------------------------- | ------------------ | ------------------- | ----------------------- |
| [ErgoDox](https://deskthority.net/wiki/ErgoDox)           |   ErgodoxEZ, Massdrop, FalbaTech, others |  USB  |     The ErgoDox is a fairly high-end NKRO keyboard at $200, with an ortholinear layout. It has two separate halves, so you can angle them to suit you. You can order it with the Gateron White keys, which have an extremely light, 35 gram activation force. Read a [guide to Starting Stenography with an Ergodox by Paul Fioravanti](https://paulfioravanti.com/blog/2018/10/18/starting-stenography-with-an-ergodox/).                    |
| [Planck](http://olkb.com/planck/) | OLKB | USB | The Planck is a fully programmable NKRO keyboard with an ortholinear layout. It is 40% the size of a standard keyboard. Read a [guide to starting stenography with a Planck by DiDoesDigital](https://didoesdigital.com/blog/build-your-own-steno-keyboard-its-easier-than-you-think/).  <br /> ![Planck steno keyboard](https://i.imgur.com/e9B2qpO.jpg)|
|[Preonic](http://olkb.com/preonic/)| OLKB | USB | The Preonic is a fully programmable NKRO keyboard with an ortholinear layout. It is 50% the size of a standard keyboard. |
| [Gherkin](http://plover.stenoknight.com/2018/05/limited-time-offer-stenogherkins-at-cost.html) | | USB | The Gherkin is a fully programmable NKRO keyboard with an ortholinear layout. It is 30% the size of a standard keyboard.

<a id="notebooks-with-nkro"></a>