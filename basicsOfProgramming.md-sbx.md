# Basics of Programming | [HOME](README.md) |
# What is Programming?

[Table of Contents](#table-of-contents "Table Of Contents")

*Programming* is a means to tell a computer (or, in the case of
the Arduino, a *microcontroller*) what to do, when to do it and how
to do it, and if to keep on doing it 'forever' or for an amount of
time, or (yup, there's more options) &hellip; until some resource
it needs (to keep running) has been completely used up.

> #### Scenario: potato-chip counting machine
> 
> *You want to build a machine that counts potato chips in your potato
chip factory.  It's a task well-suited to industrial microcontrollers,
which are smallish devices that often fit in the palm of your hand,
> for just the microcontroller 'chip' itself.*

A microcontroller is just another type of computer chip, but its
specialty is dealing with the real world, through 'mechatronics'
(electro-mechanical devices and other machinery that can accept
instructions via wires &hellip; or, in the modern day, via
wireless links).

> *So you wire it all up&hellip; your potato-chip counting
> machine&hellip; and start 'programming it'.*
> 
> *Programming&hellip; the microcontroller chip found soldered to the
target board (Arduino Uno, Leonardo, Mega2560&hellip; or
> other board).*

It'll be a chip with a part number, such as `32u4` or `328p` and
usually has branding included (`ATMega 328p`, `ATMega 32u4`) depending
on if it needs to be clarified, or if it's clear what chip is being
discussed.

> #### When you ask for help, include the model and part number
> 
> [Table of Contents](#table-of-contents "Table Of Contents")
> 
> *"I have an Uno R3 (328p) and I can compile a simple program for it,
upload the program to the Uno, and it seems to run (prints messages
> to the Serial Terminal, as expected).  But there's a problem&hellip;"*


# What, then, is Programming?

[Table of Contents](#table-of-contents "Table Of Contents")


#### Introduction for Beginners: What is a Computer Language?

[Table of Contents](#table-of-contents "Table Of Contents")

From Leo Brodie:

[Starting Forth: Introductions](
https://www.forth.com/starting-forth/0-starting-forth/)

> At first when beginners hear the term “computer language,” they
wonder, “What kind of language could a computer possibly speak? It
must be awfully hard for people to understand. It probably looks like:

> > `976#!@NX714&+`

> if it looks like anything at all.

> Actually a computer language should not be difficult to understand.
Its purpose is simply to serve as a convenient compromise for
communication between a person and a computer.

 - - -

So, looking at it from Leo's point of view, *programming* is a way to
talk to a computer.  Even the word, 'talk' is misused here&mdash;*they
had to start somewhere*.  There are many *borrow-words* used in
*programming*, taken from the learner's native (spoken and written;
human; pre-computer) language.

## Nuts and Bolts of Programs

[Table of Contents](#table-of-contents "Table Of Contents")

The microcontroller (`MCU`) chip itself accepts a long series of
`1's and 0's` (ones and zeros) as its only means of communication
(excepting analog, but that's another talk show).

The *machine code* is just those `1's and 0's` and doesn't need further
support to function.

*Assembly Language* is simply using those very same `1's and 0's`,
but with a cheater lookup table, so that you could use made-up words
to represent frequently used patterns of `1's and 0's` in your
new 'program'.

*Machine code* can be programmed using just front panel switches.
Nothing else!

![Altair 8800 from the Computer History Museum - Wikipedia](
https://upload.wikimedia.org/wikipedia/commons/thumb/0/03/Altair_8800_at_the_Computer_History_Museum%2C_cropped.jpg/1024px-Altair_8800_at_the_Computer_History_Museum%2C_cropped.jpg "8800 from the Computer History Museum - Wikipedia")

*Assembler (assembly language)* would require you to use some
kind of a typewriter&mdash;or other keyboard-like device&mdash;so
that you could use some kind of *language*&mdash;made-up, or
borrowed from someone else&mdash;to 'talk' to the microcontroller,
and give it *instructions on what to do*.

And when to do it.  How to do it!  When not to do it.  And, maybe,
special instructions on what should be done if your *assumptions
were incorrect*. ;)

### Grateful program

[Table of Contents](#table-of-contents "Table Of Contents")

**This is what a simple program might look like, in the**
***Arduino IDE*** **:**

```cpp
// #include <Arduino.h> // optional

void haha() {
    Serial.println("When I die,");
    Serial.println("Bury me deep;");
    Serial.println("Put two speakers at my feet.");
    Serial.println("Put some headphones on my head,");
    Serial.println(".. and always play the Grateful Dead.");
}

void setup() {
    Serial.begin(9600);
    haha();
    delay(2200);
}

void loop() {
    Serial.println("   Always play the Grateful Dead.");
    delay(2200);
}
```


#### Quick wokwi demo

[Table of Contents](#table-of-contents "Table Of Contents")

[*Now Playing*](https://wokwi.com/projects/346503862192964178 "Now Playing")
&nbsp;&nbsp;*on*&nbsp;&nbsp;
[*wokwi.com*](https://wokwi.com/ "wokwi.com")
&nbsp;&nbsp;&nbsp;&nbsp;*See it in action, now!*

### Ok but this got complicated, fast

[Table of Contents](#table-of-contents "Table Of Contents")

Yeah, it did. ;)

Here's a wokwi 'answer' to some of that:

[*Misuse of C Preprocessor to simplify code*](
https://wokwi.com/projects/346588077549945428)
**morse_beacon.ino** *on wokwi*

That lets you cheat, quite a bit. ;)


> *Disclaimer: the above cheat comes directly from experience in
'Forth' programming (it's another programming language).  Forth
programmers often resort to the C Preprocessor to coerce C++ program
syntax&hellip; really, quite a bit. ;)*

> *You're not 'supposed to' do this&mdash;there's a strong feeling
about this, about.  Just be aware of it; it's a large detour from
C++ itself, which is the 'Language of Arduino' so to speak.*

### Hide those details in a library

[Table of Contents](#table-of-contents "Table Of Contents")

[*Misuse Morse with Hidden Details*](
https://wokwi.com/projects/346589390531723859)
**morse_beacon_cheaty.ino** *on wokwi*


[*Misuse Morse with Beeps*](
https://wokwi.com/projects/346608451675226708)
**morse_beacon_beeps.ino** *on wokwi*


```


zork:  "You see a jelly nailed to a tree, here.  Exits: East, Up, West"


```

## The C++ Language is the language used in the Arduino IDE

[Table of Contents](#table-of-contents "Table Of Contents")

There's a 'computer language' called `C++` that is used in the
Arduino IDE, similarly to how `C++` is used on your desktop PC.

Most of what's in this document (the one you're reading right
now) uses `code examples` written for the Arduino IDE, using
specifics of the 'Arduino Language' as it were.

You can take a look here, for some of the basics of that language:

[Arduino IDE Language Reference](
https://www.arduino.cc/reference/en/)


## Tools, not Rules

[Table of Contents](#toc-tools-not-rules "Table Of Contents")

### Top down, bottom up, middle out

[Table of Contents](#toc-tools-not-rules "Table Of Contents")

So, the above program already *works*.  Here's a way to look at how
it got made (see just below).

```cpp
#include <Arduino.h>
void setup() { } void loop() {} // END.
```

This program compiles and 'runs' just fine, on wowki.  Doesn't do
much; isn't meant to.

In a sense, it has several *placeholders* for *future ideas* that
were not (yet) typed into the computer (using some kind of
*code editor* or just a *plaintext* editor).


> *If you leave a placeholder in, 'permanently', you have just
> created a* **hook**.  *Do not put in hooks.  Ever.  Create them
> as required.*

> *If you must, revision control has tools to help you remember
> how to add the hook, when it is truly wanted.*

**The above is opinion, and isn't to be followed; unless you agree
to it by your own philosophy.** &nbsp;&nbsp;&nbsp;;)


`/netreligion`


`Top-down, bottom-up, middle-out` is an approach to programming; it
surely has an accepted definition and description, but will be used
here, only informally, to describe what the theory books will talk
about in detail, using proper names for everything. ;)

It's a tool.  You can use it, or fall back on your other skills and
completely ignore it.  *Everyone develops a style of their own*.

[Table of Contents](#toc-tools-not-rules "Table Of Contents")

```cpp
#include <Arduino.h>

void setup() {
}

void loop() {
}

// END.
```

*Slightly more formal - same exact program; just added some spacing
to make it a bit easier to take in, while reading it over.*

### Initialize the Serial stuph

[Table of Contents](#toc-tools-not-rules "Table Of Contents")

```cpp
#include <Arduino.h>

void setup() {
    Serial.begin(9600);
}

void loop() {
}

// END.
```

### Add a placeholder function called `haha()`

&hellip; that will (later on) contain something interesting to do,
after starting the Serial going (which lets you print stuph out).

[Table of Contents](#toc-tools-not-rules "Table Of Contents")

```cpp
#include <Arduino.h>

void haha() { }

void setup() {
    Serial.begin(9600);
    haha();
}

void loop() {
}

// END.
```

### Make `haha()` do something slightly interesting. Then test it

[Table of Contents](#toc-tools-not-rules "Table Of Contents")


```cpp
#include <Arduino.h>

void haha() {
    Serial.println(" TEST abciq "); // weird message to recognize as ours
}

void setup() {
    Serial.begin(9600);
    haha();
}

void loop() {
}

// END.
```

### It's working

[Table of Contents](#toc-tools-not-rules "Table Of Contents")

```cpp

#include <Arduino.h>

void haha() {
    Serial.println("When I die,");
    Serial.println("Bury me deep;");
    Serial.println("Put two speakers at my feet.");
    Serial.println("Put some headphones on my head,");
    Serial.println(".. and always play the Grateful Dead.");
}

void haha_old_delete_me() { // cruft
    Serial.println(" TEST abciq "); // weird message
}

void setup() {
    Serial.begin(9600);
    haha();
}

void loop() {
}

// END.
```

So the program's 'working'.  People say that a
lot:&nbsp;&nbsp;&nbsp;*"It's working."* &nbsp;&nbsp;;)

**Better:** It compiles.  It mostly does what was expected.  Does at
least something useful.  Doesn't quite do what was in mind when
it was first *edited as code*.


### Comment out unused code

[Table of Contents](#toc-tools-not-rules "Table Of Contents")

```cpp

#include <Arduino.h>

void haha() {
    Serial.println("When I die,");
    Serial.println("Bury me deep;");
    Serial.println("Put two speakers at my feet.");
    Serial.println("Put some headphones on my head,");
    Serial.println(".. and always play the Grateful Dead.");
}

#if 0
void haha_old_delete_me() { // cruft
    Serial.priantln(" TEST abciq "); // weird message
}
#endif

void setup() {
    Serial.begin(9600);
    haha();
}

void loop() {
}

// END.
```

*Shows a method for commenting-out code that does not spoil syntax
highlighting inside the commented code.*

Note that `Serial.priantln("message");` is deliberately misspelled,
but still 'compiles clean'.

*That was a test of the `#if 0` &hellip; `#endif`
construct.* &nbsp;&nbsp;;)


### Strip out commented code entirely

[Table of Contents](#toc-tools-not-rules "Table Of Contents")

```cpp

#include <Arduino.h>

void haha() {
    Serial.println("When I die,");
    Serial.println("Bury me deep;");
    Serial.println("Put two speakers at my feet.");
    Serial.println("Put some headphones on my head,");
    Serial.println(".. and always play the Grateful Dead.");
}

void setup() {
    Serial.begin(9600);
    haha();
}

void loop() {
}

// END.
```

*Code clean-up - the commented code is no longer operative
and is removed.  Don't worry, with revision control, it is
easily recalled, as required.*

### What still remains to be done - snippet

[Table of Contents](#toc-tools-not-rules "Table Of Contents")

```cpp
// - - -  CODE SNIPPET - - - DOES NOT COMPILE - - -

void setup() {
    Serial.begin(9600);
    haha();
    delay(2200);
}

void loop() {
    Serial.println("   Always play the Grateful Dead.");
    delay(2200);
}
```

This is really what's left to be done; *taken from the working
program; scroll up to see it.*


### Add the repeating code to the loop

[Table of Contents](#toc-tools-not-rules "Table Of Contents")

```cpp

#include <Arduino.h>

void haha() {
    Serial.println("When I die,");
    Serial.println("Bury me deep;");
    Serial.println("Put two speakers at my feet.");
    Serial.println("Put some headphones on my head,");
    Serial.println(".. and always play the Grateful Dead.");
}

void setup() {
    Serial.begin(9600);
    haha();
}

void loop() {
    Serial.println("   Always play the Grateful Dead.");
    delay(2200);
}

// END.
```

*Now the loop is 'playing'.  It's got stuph inside of it.
And it does it, whatever is in there, repeatedly.*


### Fixup the `setup()` to separate events

[Table of Contents](#toc-tools-not-rules "Table Of Contents")

```cpp

#include <Arduino.h>

void haha() {
    Serial.println("When I die,");
    Serial.println("Bury me deep;");
    Serial.println("Put two speakers at my feet.");
    Serial.println("Put some headphones on my head,");
    Serial.println(".. and always play the Grateful Dead.");
}

void setup() {
    Serial.begin(9600);
    haha();
    delay(2200);
}

void loop() {
    Serial.println("   Always play the Grateful Dead.");
    delay(2200);
}

// END.
```

*A slight refinement: there's a decently long delay after
the `haha()` message plays, marking distinctly where the
`setup()` and and where the `loop()` begins, without
crudding it up with a `Mr. Obvious` announcement such as
`You are entering the loop!`*



## Blink with Weight

[Table of Contents](#toc-blink-with-weight "Table Of Contents")

[*Blink With Weight*](
https://wokwi.com/projects/346778138320044627)
**blink_with_weight.ino** *on wokwi*

(Scroll for discussion)

`The code:`

```cpp
// https://wokwi.com/projects/346778138320044627

// Fri 28 Oct 16:03:11 UTC 2022

// Blink an LED, over and over ('endless loop')

void LED_ON() {
  digitalWrite(LED_BUILTIN, 1);
}

void LED_OFF() {
  digitalWrite(LED_BUILTIN, 0);
}

// ON_TIME  200     OFF_TIME  1000

//  WEIGHT    5     UNIT_TIME    4
//   SCALE   50

#define WEIGHT 5 // OFF to ON ratio (time intervals)
                 // larger WEIGHT gives more OFF time
#define UNIT_TIME 4 // basis of all other timings
#define SCALE 50 // scales all times evenly

#define ON_TIME (UNIT_TIME * SCALE)
#define OFF_TIME (ON_TIME * WEIGHT)

void report() {
  Serial.println("\n The red LED is marked 'L' on the Uno.");
  Serial.println(" This program makes it blink.");

  Serial.print("\n Your ON_TIME: ");
  Serial.print(ON_TIME);
  Serial.print("    Your OFF_TIME: ");
  Serial.println(OFF_TIME);
  Serial.println("");
}


void LED_BLINK () {
  LED_ON();
  delay(ON_TIME);
  LED_OFF();
  delay(OFF_TIME);
}

void setup_GPIO() {
  pinMode(LED_BUILTIN, OUTPUT);
  LED_OFF();
}

void setup_serial() {
  Serial.begin(9600);
}

void setup() {
  setup_GPIO();
  setup_serial();
  report();
}

void loop() {
  LED_BLINK();
}

// END.
```
### Blink with Weight - first simplification

[Table of Contents](#toc-blink-with-weight "Table Of Contents")

*Can you simplify that, slightly?*

Sure:


```
 $ cpp ./code.cpp > preprocessed-code.cpp
 $ cat ./preprocessed-code.cpp
```

```cpp
void LED_ON() {
  digitalWrite(LED_BUILTIN, 1);
}

void LED_OFF() {
  digitalWrite(LED_BUILTIN, 0);
}

void report() {
  Serial.println("\n The red LED is marked 'L' on the Uno.");
  Serial.println(" This program makes it blink.");

  Serial.print("\n Your ON_TIME: ");
  Serial.print((4 * 50));
  Serial.print("    Your OFF_TIME: ");
  Serial.println(((4 * 50) * 5));
  Serial.println("");
}

void LED_BLINK () {
  LED_ON();
  delay((4 * 50));
  LED_OFF();
  delay(((4 * 50) * 5));
}

void setup_GPIO() {
  pinMode(LED_BUILTIN, OUTPUT);
  LED_OFF();
}

void setup_serial() {
  Serial.begin(9600);
}

void setup() {
  setup_GPIO();
  setup_serial();
  report();
}

void loop() {
  LED_BLINK();
}
// END.
```

### Blink with Weight - first simplification - discussion

[Table of Contents](#toc-blink-with-weight "Table Of Contents")

*You said it was simpler, but there's new stuff now!*

Yeah.

The **C Preprocessor** was used to 'process' all the `#define` stuff.

What it does is **substitute** what you would have typed by hand if
you had never used a `#define` at all (for this use; there are other
interesting uses for a `#define` that are different from this use!)

In this case, the original `#define` statements, some of them, were
not simple substitutions of number.  Instead, they substituted
multiplications, with the parentheses, and 'typed them into' the
main program text, exactly as you could have done yourself, by hand.

The C Preprocessor did not simplify further, so all the parentheses
are intact.

You can simplify further on your own, if you want simpler, hard-
coded numbers where the multiplications went.

That'll be next:


### Factor - remove determinant math

[Table of Contents](#toc-blink-with-weight "Table Of Contents")

```cpp
void LED_ON() {
  digitalWrite(LED_BUILTIN, 1);
}

void LED_OFF() {
  digitalWrite(LED_BUILTIN, 0);
}

void report() {
  Serial.println("\n The red LED is marked 'L' on the Uno.");
  Serial.println(" This program makes it blink.");

  Serial.print("\n Your ON_TIME: ");
  Serial.print(200);    // 4 * 50 = 200
  Serial.print("    Your OFF_TIME: ");
  Serial.println(1000); // 4 * 50 * 5 = 1000
  Serial.println("");
}

void LED_BLINK () {
  LED_ON();
  delay(200);  // 4 * 50 = 200
  LED_OFF();
  delay(1000); // 4 * 50 * 5 = 1000
}

void setup_GPIO() {
  pinMode(LED_BUILTIN, OUTPUT);
  LED_OFF();
}

void setup_serial() {
  Serial.begin(9600);
}

void setup() {
  setup_GPIO();
  setup_serial();
  report();
}

void loop() {
  LED_BLINK();
}
// END.
```

*It's a bit simpler, now.*

#### What changed: second simplification of Blink with Weight

[Table of Contents](#toc-blink-with-weight "Table Of Contents")

 * The C Preprocessor directives are gone (no more `#define`)
 * The math inside the parentheses was done by hand, and the results
   were substituted

#### What was lost in the process of simplification

[Table of Contents](#toc-blink-with-weight "Table Of Contents")

 * The individual numbers that make up the math had real value, to
   change timing of the LED `blink/dark` cycle.
 * Those timings were distinct and could be easily changed when they
   were still part of the `#define` statements; that ease of
   use/change/experimentation is no longer as evident.

### Third simplification - Blink with Weight

[Table of Contents](#toc-blink-with-weight "Table Of Contents")

**Compress the code - LED_BLINK() - i**

```cpp
void xxxLED_ON() {
  digitalWrite(LED_BUILTIN, 1);
}

void xxxLED_OFF() {
  digitalWrite(LED_BUILTIN, 0);
}

void report() {
  Serial.println("\n The red LED is marked 'L' on the Uno.");
  Serial.println(" This program makes it blink.");

  Serial.print("\n Your ON_TIME: ");
  Serial.print(200);    // 4 * 50 = 200
  Serial.print("    Your OFF_TIME: ");
  Serial.println(1000); // 4 * 50 * 5 = 1000
  Serial.println("");
}

void LED_BLINK () {
  // LED_ON();
  digitalWrite(LED_BUILTIN, 1);
  delay(200);  // 4 * 50 = 200
  // LED_OFF();
  digitalWrite(LED_BUILTIN, 0);
  delay(1000); // 4 * 50 * 5 = 1000
}

void setup_GPIO() {
  pinMode(LED_BUILTIN, OUTPUT);
  // LED_OFF();
}

void setup_serial() {
  Serial.begin(9600);
}

void setup() {
  setup_GPIO();
  setup_serial();
  report();
}

void loop() {
  LED_BLINK();
}
// END.
```

### Remove the commented code and comment out the unused functions

[Table of Contents](#toc-blink-with-weight "Table Of Contents")

**Compress the code - LED_BLINK() - ii**

```cpp
// void xxxLED_ON() {
  // digitalWrite(LED_BUILTIN, 1);
// }

// void xxxLED_OFF() {
  // digitalWrite(LED_BUILTIN, 0);
// }

void report() {
  Serial.println("\n The red LED is marked 'L' on the Uno.");
  Serial.println(" This program makes it blink.");

  Serial.print("\n Your ON_TIME: ");
  Serial.print(200);
  Serial.print("    Your OFF_TIME: ");
  Serial.println(1000);
  Serial.println("");
}

void LED_BLINK () {
  digitalWrite(LED_BUILTIN, 1);
  delay(200);
  digitalWrite(LED_BUILTIN, 0);
  delay(1000);
}

void setup_GPIO() {
  pinMode(LED_BUILTIN, OUTPUT);
}

void setup_serial() {
  Serial.begin(9600);
}

void setup() {
  setup_GPIO();
  setup_serial();
  report();
}

void loop() {
  LED_BLINK();
}
// END.
```

*Good.  Still runs exactly the same; code is a bit 'simpler' now.*

*Not necessarily 'better' but it is simpler!*


### Cram it all into setup() where it was split out into functions

[Table of Contents](#toc-blink-with-weight "Table Of Contents")

**Compress the code - setup() - i**

```cpp
void LED_BLINK () {
  digitalWrite(LED_BUILTIN, 1);
  delay(200);
  digitalWrite(LED_BUILTIN, 0);
  delay(1000);
}

void setup() {
  // setup_GPIO();
  pinMode(LED_BUILTIN, OUTPUT);

  // setup_serial();
  Serial.begin(9600);

  // report();
  Serial.println("\n The red LED is marked 'L' on the Uno.");
  Serial.println(" This program makes it blink.");

  Serial.print("\n Your ON_TIME: ");
  Serial.print(200);
  Serial.print("    Your OFF_TIME: ");
  Serial.println(1000);
  Serial.println("");
}

void loop() {
  LED_BLINK();
}
// END.
```


### Druids, man.

[Table of Contents](#toc-adruids-man "Table Of Contents")

*Nope. ;)*

**Compress the code - setup() - ii**

```cpp
void LED_BLINK () {
  digitalWrite(LED_BUILTIN, 1); delay(200);
  digitalWrite(LED_BUILTIN, 0); delay(1000);
}

void setup() {
  pinMode(LED_BUILTIN, OUTPUT);
  Serial.begin(9600);
  Serial.print("\n ON: "); Serial.print(200);
  Serial.print("    OFF: "); Serial.println(1000);
  Serial.println("");
}

void loop() {
  LED_BLINK();
}
// END.
```

*Made things a bit more compact; the essential LED blink rate and
duty cycle are unchanged.*

`report()` remnants greatly reduced or compressed to simpler
information printed.

*Note that the `delay()` statements were brought up to the same
lines as the `digitalWrite()` statements, saving on some vertical
space.  There was a lot of unused empty space, there, and the
clarity of the code doesn't suffer much (if at all) to do it
that way.*


### Last simplification: no printing at all.

[Table of Contents](#toc-adruids-man "Table Of Contents")

*Maybe you don't have printing working, anyway, and already
know enough without the printing statements.*

**Compress the code - no printing at all**

```cpp
void LED_blink () {
  digitalWrite(LED_BUILTIN, 1); delay(200);
  digitalWrite(LED_BUILTIN, 0); delay(1000);
}

void setup() {
  pinMode(LED_BUILTIN, OUTPUT);
}

void loop() {
  LED_blink();
}
```

*Also renamed the LED_BLINK() function to get rid of the excess
upper-case lettering.*


### Wait wait can't you just shove it in the loop?

[Table of Contents](#toc-adruids-man "Table Of Contents")

*You're right!  Missed that simplification. ;*

**Compress the code - everything inside the loop()**

```cpp
void setup() {
  pinMode(LED_BUILTIN, OUTPUT);
}

void loop() {
  digitalWrite(LED_BUILTIN, 1); delay(200);
  digitalWrite(LED_BUILTIN, 0); delay(1000);
}
```


### Okay that was a bit too stingy, what about making it look nice, again?

[Table of Contents](#toc-adruids-man "Table Of Contents")

*Good idea.*

&nbsp;&nbsp;&nbsp;&nbsp;**Compress the code - reformat for clarity
and simplicity**

```cpp
void setup() {
    pinMode(LED_BUILTIN, OUTPUT);
}

void loop() {
    digitalWrite(LED_BUILTIN, 1);
    delay(200);

    digitalWrite(LED_BUILTIN, 0);
    delay(1000);
}
```

**That's kinda nice now!**

Indeed.


## Discussion - Blink with Weight - LED blinker program

[Table of Contents](#toc-adruids-man "Table Of Contents")

*led blinker*

*The discussion itself goes here.*

## Pseudocode

[Table of Contents](#toc-adruids-man "Table Of Contents")

#### What's pseudocode?

*Pseudocode is code you write without obeying real syntax rules;
it's there for you, and is meant to remind you of something pretty
close to what you wanted to 'program into the microcontroller' at
some point (hopefully later today!)*

That's pretty much it: fake code that is meant to *model* what you
think should be *going on* in your *program* when it's either
*finished* or at least *completed, up to a certain point* in
its *development*.

## Arduino IDE

[Table of Contents](#toc-arduino-ide "Table Of Contents")

The **Arduino IDE** looks like this, when you are about to compile
a program:

![image](images/basicsOfProgramming/arduino_IDE-b.jpg)

### Program Listing - sketch_oct31a.ino

[Table of Contents](#toc-arduino-ide "Table Of Contents")

```cpp
void setup() {
  // put your setup code here, to run once:
  pinMode(LED_BUILTIN, OUTPUT);
}

void loop() {
  // put your main code here, to run repeatedly:
  digitalWrite(LED_BUILTIN, 1);
  delay(200);

  digitalWrite(LED_BUILTIN, 0);
  delay(1000);
}
// END.
```

You can use **Control + R** to `Verify/Compile` your program.

This simply means you'll be invoking the `compiler`, which will take
the code you have in the upper Arduino IDE window, and try to turn
what you've written into the `1's and 0's` that the Arduino Uno (or
other target board) can use as its 'program'.

This program is often called the `firmware` which resides in the
`flashROM` of the `target MCU` *(microcontroller)* once it has been
`uploaded` to your Uno (or other board).

**You must pick a board and compile just for that board** to
succeed, here.

Now it is true that many small programs that you'll write will
compile, unmodified, for quite a few different Arduino boards,
as well as for (almost) countless `third-party vendor` boards.

*The above code 'worked' on **wokwi.com** for their Uno, ATMEGA 2560
and at least one other board listed there.  Unmodified.  Most boards
that have an LED on the board itself (for a 
[**blinkenlight**](https://en.wikipedia.org/wiki/Blinkenlights))
will have a definition for LED_BUILTIN that will operate that LED
without knowing its 'proper' port pin number (it's usually
on `D13`).*

Some boards only have an `RGB` LED, which needs a completely different
approach to get it to work (at all).

Old school LEDs just need power (and a series, current-limiting
resistor) to operate, so those are great for simple testing.  The
above program uses one of those (as the Uno has one soldered onto
it, permanently).

*If your board only has an `RGB` LED, you'll need to connect a single,
old school LED, with a series resistor (about 1k Ohms) to one of the
`port pins` of your board, to blink it.*

#### void setup()

[Table of Contents](#toc-arduino-ide "Table Of Contents")

This declares there's a `function` named `setup()` to be `compiled`
into the program.

It `returns` nothing when called, and so gets a `type` of `void`.

Other functions may also be declared `void`&mdash;they return
nothing, but simply `execute` (or 'run') if `called` (almost
always, from inside another `function`).

*`setup()` does just what it sounds like&mdash;it sets up your
program's starting conditions.*

Pragmatically, `setup()` executes only once during the entire
time your program is running&mdash;pretty much 'just after'
power was applied to your board.

*See the discussion on `main()` for a bit more context.*


#### void loop()

[Table of Contents](#toc-arduino-ide "Table Of Contents")

Same idea as `void setup()`&hellip; only this time, the function
automatically repeats ('forever') when called.

***Any function can behave as a `loop`*** if constructed properly.
This is quite common.

`loop()` is the only function in the Arduino IDE that loops without
explicit 'looping' code structure.

*`setup()` and `loop()` are usually required by the Arduino IDE.*


#### int main(void)

[Table of Contents](#toc-arduino-ide "Table Of Contents")

In the Arduino IDE, a specially-named function, `int main(void)`
gets called automatically, to start the program.

You do not usually call `main()` in your code; it's specified
(already) in a file named `main.cpp` in the Arduino IDE.

See [main.cpp](https://github.com/arduino/ArduinoCore-avr/blob/master/cores/arduino/main.cpp) *(also shown below)*.

Traditional programs use `main()` to start things; the Arduino IDE
also (optionally) allows you to do so, but encourages you (instead)
to use `setup()` and `loop()`.

*If you don't already know `C/C++` and are learning on the Arduino
IDE, this brief introduction to `main()` isn't likely to be important
to you&mdash; it's here mostly to help `C/C++` programmers new to the
Arduino IDE to understand what's happening with the requirements of
`setup()` and `loop()`.*

Here it is:

```
int main(void)
{
    init();

    initVariant();

#if defined(USBCON)
    USBDevice.attach();
#endif

    setup();

    for (;;) {
        loop();
        if (serialEventRun) serialEventRun();
    }

    return 0;
}
```

***This is where `setup()` and `loop()` and their mandatory natures
are apparent.***

The `for (;;)` construct is a simple counted loop mechanism, with no
counting.  The syntax used specifies *'Yes, loop in a counting way,
but do not count&mdash;treat as if the count were somehow 'infinite'
and behave similarly to a proper, counted loop.'*


### Firmware upload

[Table of Contents](#toc-arduino-ide "Table Of Contents")

Use **Control + U** to `Upload` the compiled `sketch` (program) to
your target board (Uno, or other board).

> *That stays the same no matter how different your board is
> from the more usual ones - `Control R` and `Control U` work
> with any board supported.*

Many boards use **`avrdude`** or **`bossac`** to **upload**
the 'compiled' program&hellip; the `1's and 0's` mentioned
in this document.

**`avrdude`** is used for the Uno and for most (or all)
**AVR** boards.

*AVR boards are `8-bit` boards, which (among other things) means the
native storage system they use is eight bits wide.  Just about all
8-bit boards have a relatively small working memory complement (512
bytes to about 3072 bytes).  Their `mass storage` complement is
around 4 kilobytes to about 64 kilobytes.*

`16-bit boards` are rare.

**`32-bit boards`** (`Due`, `mkr series`, `M0 Pro` and many others)
**are not AVR boards** and usually use **`bossac`** to do the
**uploading**.  They have a lot more working memory than the AVRs,
and their programs can be correspondingly larger.

For example, SAMD21E18A is a low-end SAMD21 variant (G18A is standard).
It has 256k flash (mass storage) and 32k RAM (working memory) on the
chip itself.

Many (most) 32-bit MCU boards use the **`ARM Cortex`** series of
MCU chips.

`bossac` is the usual tool, to send firmware (usually via USB) to
most **ARM Cortex** and other 32-bit boards that have Arduino IDE
support (sometimes called *board support packages*).

### Board Support Packages

[Table of Contents](#toc-arduino-ide "Table Of Contents")

Boards don't necessarily have support from the Arduino IDE, as you
first install it.  There are several boards that are included; the
Uno is the factory default.

*You could buy an Uno R3, download the Arduino IDE, write a very
simple program, compile it and upload it to the Uno, all without
changing much of anything in the Arduino IDE's menu system.*

### Sketchbook

[Table of Contents](#toc-arduino-ide "Table Of Contents")

The Arduino IDE calls the directory where your programs are stored
the `Sketchbook`.  It is found in the menu system, following a
**File > Sketchbook** menu sequence.

### Themes

[Table of Contents](#toc-arduino-ide "Table Of Contents")

You can have a single theme for the Arduino IDE in a directory
named 'theme' in your `Sketchbook`.

> OS-dependent: The `Sketchbook` is usually/always named
> `'~/Arduino'` in Linux; the theme directory for Linux is named
> `'~/Arduino/theme'` and does not exist after installation of
> the Arduino IDE, as it is optional.

Copy all the files from:

[theme](https://github.com/arduino/Arduino/tree/master/build/shared/lib/theme)

to a directory named `theme` in your `Sketchbook` folder, and
modify to suit.

[theme.txt](images/basicsOfProgramming/sequoia/theme.txt)
has been modified to show possible changes, as a quick example.

If you have multiple themes, zip each one up without including
creation of a directory (when it is unzipped, it will not create a
new directory to hold the newly-unzipped .ZIP archive; instead,
it unzips in whatever is the current directory - at least, under
Linux, that's true).

Then drop all the .ZIP files into the `'~/Arduino/theme'` directory.
From there, **File > Preferences** will offer a means to choose one
of them over the others.

**As is usual** for the Arduino IDE, always restart it (exit it
entirely, then start it afresh) after changing a Preference.

***For a single .ZIP theme:***  Just unzip it in your theme directory
in the `Sketchbook`.  The .ZIP creates one directory (`'syntax/'`),
but most of the theme's files are in the base ('theme') directory,
for a single theme installation.

Table of Contents
=================

- [Basics of Programming | HOME |](#basics-of-programming--home-)
- [What is Programming?](#what-is-programming)
  - [Scenario: potato-chip counting machine](#scenario-potato-chip-counting-machine)
  - [When you ask for help, include the model and part number](#when-you-ask-for-help-include-the-model-and-part-number)

- [What, then, is Programming?](#what-then-is-programming)
      - [Introduction for Beginners: What is a Computer Language?](#introduction-for-beginners-what-is-a-computer-language)
  - [Nuts and Bolts of Programs](#nuts-and-bolts-of-programs)
    - [Grateful program](#grateful-program)
      - [Quick wokwi demo](#quick-wokwi-demo)
    - [Ok but this got complicated, fast](#ok-but-this-got-complicated-fast)
    - [Hide those details in a library](#hide-those-details-in-a-library)

  - [The C++ Language is the language used in the Arduino IDE](
    #the-c-language-is-the-language-used-in-the-arduino-ide)

    <a name="toc-tools-not-rules"></a>
  - [Tools, not Rules](#tools-not-rules)
    - [Top down, bottom up, middle out](#top-down-bottom-up-middle-out)
    - [Initialize the Serial stuph](#initialize-the-serial-stuph)
    - [Add a placeholder function called `haha()`](#add-a-placeholder-function-called-haha)
    - [Make `haha()` do something slightly interesting. Then test it](#make-haha-do-something-slightly-interesting-then-test-it)
    - [It's working](#its-working)
    - [Comment out unused code](#comment-out-unused-code)
    - [Strip out commented code entirely](#strip-out-commented-code-entirely)
    - [What still remains to be done - snippet](#what-still-remains-to-be-done---snippet)
    - [Add the repeating code to the loop](#add-the-repeating-code-to-the-loop)
    - [Fixup the `setup()` to separate events](#fixup-the-setup-to-separate-events)
    <a name="toc-blink-with-weight"></a>
  - [Blink with Weight](#blink-with-weight)
    - [Blink with Weight - first simplification](#blink-with-weight---first-simplification)
    - [Blink with Weight - first simplification - discussion](#blink-with-weight---first-simplification---discussion)
    - [Factor - remove determinant math](#factor---remove-determinant-math)
      - [What changed: second simplification of Blink with Weight](#what-changed-second-simplification-of-blink-with-weight)
      - [What was lost in the process of simplification](#what-was-lost-in-the-process-of-simplification)
    - [Third simplification - Blink with Weight](#third-simplification---blink-with-weight)
    - [Remove the commented code and comment out the unused functions](#remove-the-commented-code-and-comment-out-the-unused-functions)
    - [Cram it all into setup() where it was split out into functions](#cram-it-all-into-setup-where-it-was-split-out-into-functions)
      <a name="toc-adruids-man"></a>
    - [Druids, man.](#druids-man)
    - [Last simplification: no printing at all.](#last-simplification-no-printing-at-all)
    - [Wait wait can't you just shove it in the loop?](#wait-wait-cant-you-just-shove-it-in-the-loop)
    - [Okay that was a bit too stingy, what about making it look nice, again?](#okay-that-was-a-bit-too-stingy-what-about-making-it-look-nice-again)
  - [Discussion - Blink with Weight - LED blinker program](#discussion---blink-with-weight---led-blinker-program)
  - [Pseudocode](#pseudocode)
    <a name="toc-arduino-ide"></a>
  - [Arduino IDE](#arduino-ide)
    - [Program Listing - sketch_oct31a.ino](#program-listing---sketch_oct31aino)
    - [void setup()](#void-setup)
    - [void loop()](#void-loop)
    - [int main(void)](#int-mainvoid)
    - [Firmware upload](#firmware-upload)
    - [Board Support Packages](#board-support-packages)
    - [Sketchbook](#sketchbook)
    - [Themes](#themes)

<!-- Created by https://github.com/ekalinin/github-markdown-toc -->

<!--
`1234567890123456789012345678901234567890123456789012345678901234567..]..345`
-->

**DRAFT ONLY - INCOMPLETE**

**Fri  4 Nov 11:53:39 UTC 2022** - *timestamp only occasionally maintained ;)*

#### END.
