<!--*- mode:markdown;mode:orgtbl -*-->
# Keymacs — the keyboard layout for Emacs users

## Project targets

* Fix QWERTY problems (apply solutions from well known alternative
  layouts).
* Place keys for general Emacs combos into easily accessible places
  instead of remapping them in Emacs.

### Problems with familiar keys bindings in alternative keyboards

Commonly the most of alternative layouts solve only first problem
mentioned above: they help you avoid ergonomic problems of QWERTY. But
they are require you remap the most of frequently used in Emacs keys
because these layouts was made without Emacs in mind. For example
several well known layouts try to keep `XCV` keys in the same place as
QWERTY because historically many applications on the desktop platforms
(Windows, Mac, Linux) had used these keys for clipboard operations. So
this is a strong habit of computer users that even alternative layouts
wont break it. But Emacs uses other keys for clipboard by default:
`Ctl`-`W` for cut, `Meta`-`W` for copy and `Ctl`-`Y` for insert. I
think these keys badly placed on QWERTY. But on Dvorak layout they
placed even worse on my sense. Norman layout places them in more
accessible places though. But anyway alternative layouts targeted at
mostly used apps (like word processors and well known browsers) those
keyboard combos very different from habits suggested by Emacs. So my
try is create the layout oriented primarily on Emacs experience.

The same problem appears for Emacs navigation keys on alternative
layouts. So if you want to use better keyboard layout you will need
adapt for the layout all your Emacs bindings and bindings in the
applications that use Emacs-like bindings (shell for example).

## Application oriented layout

I think the usable keyboard layout for all purposes is a mythical idea
similar to idea of the universal programming language. A degree of
usability always depends on UI of applications you use. Different apps
have different frequency of key combinations and provide different
hotkeys.  Human languages beside English increase complexity of this
task by adding their own rules of keys frequency that unique per each
language. Also the hardware limits of common keyboards prevent to use
them ergonomically (there are a very small set of keyboards that may
be called really ergonomic).

But I think with all these limitations in mind it is possible to
increase usability of your keyboard for the applications that we use
most often for the one selected natural language. So the results for
example for a person who most of the time write texts and
presentations in office applications under MacOS will totally
different against programmer who most of the time uses Vim and text
utilities under Linux. There are no common optimal keyboard layout for
them. But when people use nearly same set of applications and speak
the same language then layouts would be similar too. So it is main
idea of this project — *it is not possible get universal ergonomic
layout for all purposes* but it possible to make *nearly ergonomic
layout* for the people who uses *the same tools*.

It main cause why I not use one of ready alternatives and research for
my own solution. In my everyday work of computer I use GNU/Emacs and
terminals with Emacs-like keybindings. I also try to set Emacs
keybindings in other programs where possible.  And most of time I
wrote texts in English for programming languages and documentation.
So with Keymacs I could get layout better for many parameters than
QWERTY and get keys placement well suited for Emacs bindings.

So it is chance that if you use Emacs and apps with Emacs-like
bindings then my keyboard layout may be good for you too.

![Keymacs layout](keymacs-layout.png)

### Factors that taken into account

* Preferable usage of the home row
* Use English letter frequency statistics
* Minimize lateral movement on the most used bigrams and trigrams
* Minimize same finger usage on the most used bigrams and trigrams
* Equal effort for both hands

### Heatmaps

There are results from [patorjk.com/keyboard-layout-analyzer](http://patorjk.com/keyboard-layout-analyzer/) for
the configuration [keyboard-analyzer-config.json](keyboard-analyzer-config.json):

![Keymacs heatmap for I chapter of "Alice in Wonderland"](keymacs-heatmap-for-alice-in-wonderland.png)

Compare with QWERTY layout:

![QWERTY heatmap for I chapter of "Alice in Wonderland"](qwerty-heatmap-for-alice-in-wonderland.png)

### Top of the most frequent n-grams in English texts

The table below consists of bigrams
[sorted by popularity in English texts](http://homepages.math.uic.edu/~leon/mcs425-s08/handouts/char_freq2.pdf).
Columns for Keymacs, Norman and QWERTY layouts reflect two aspects:

* the letters placed in Home Row
* the letters didn't require finger movement

If the condition for the layout succeeded then it marked with X. So
compare number of X marks (more is better) for Keymacs well known
layouts.

<!--- BEGIN RECEIVE ORGTBL bigrams -->
| Bigram | Keymacs | Norman | Colemak | Dvorak |
|---|---|---|---|---|
| TH | X | X |  | X |
| HE | X | X |  | X |
| AN | X | X | X | X |
| IN | X | X | X | X |
| ER | X |  | X |  |
| ND |  |  |  |  |
| RE | X |  | X |  |
| ED |  |  |  |  |
| ES |  | X | X | X |
| OU |  |  |  | X |
| TO | X | X | X | X |
| HA | X | X |  | X |
<!--- END RECEIVE ORGTBL bigrams -->

<!---
#+ORGTBL: SEND bigrams orgtbl-to-gfm
| Bigram | Keymacs | Norman | Colemak | Dvorak |
|--------+---------+--------+---------+--------|
| TH     | X       | X      |         | X      |
| HE     | X       | X      |         | X      |
| AN     | X       | X      | X       | X      |
| IN     | X       | X      | X       | X      |
| ER     | X       |        | X       |        |
| ND     |         |        |         |        |
| RE     | X       |        | X       |        |
| ED     |         |        |         |        |
| ES     |         | X      | X       | X      |
| OU     |         |        |         | X      |
| TO     | X       | X      | X       | X      |
| HA     | X       | X      |         | X      |
-->

So in Keymacs 8/12 of the most frequent bigrams placed in home row
without finger movement. Programmer Dvorak has the same result for
the finger movement.

QWERTY is the worst case with the finger movement reqiured for all
mentioned bigrams. It has not any frequent bigram in home row.

The same for the most frequent trigrams:

<!--- BEGIN RECEIVE ORGTBL trigrams -->
| Trigram | Keymacs | Norman | Colemak | Dvorak |
|---|---|---|---|---|
| THE | X | X |  | X |
| AND |  |  |  |  |
| ING |  |  |  |  |
| HER | X |  |  |  |
| HAT | X | X |  | X |
| HIS |  | X |  |  |
| THA | X | X |  | X |
| ERE | X |  | X |  |
| FOR |  |  |  |  |
| ENT | X | X |  | X |
| ION | X | X | X |  |
| TER | X |  | X |  |
<!--- END RECEIVE ORGTBL trigrams -->

<!---
#+ORGTBL: SEND trigrams orgtbl-to-gfm
| Trigram | Keymacs | Norman | Colemak | Dvorak |
|---------+---------+--------+---------+--------|
| THE     | X       | X      |         | X      |
| AND     |         |        |         |        |
| ING     |         |        |         |        |
| HER     | X       |        |         |        |
| HAT     | X       | X      |         | X      |
| HIS     |         | X      |         |        |
| THA     | X       | X      |         | X      |
| ERE     | X       |        | X       |        |
| FOR     |         |        |         |        |
| ENT     | X       | X      |         | X      |
| ION     | X       | X      | X       |        |
| TER     | X       |        | X       |        |
-->

In Keymacs 8/12 of the most frequent trigrams placed in home row
without finger movement. Other compared layouts have lesser trigrams
in home row.

QWERTY is the worst case with the finger movement reqiured for all
mentioned trigrams. It has none frequent trigrams in home row.

At last results for the most frequent quadrigrams:

<!--- BEGIN RECEIVE ORGTBL quadrigrams -->
| Quadrigram | Keymacs | Norman | Colemak | Dvorak |
|---|---|---|---|---|
| THAT | X | X |  | X |
| THER | X |  |  |  |
| WITH |  |  |  |  |
| TION | X | X | X |  |
| HERE | X |  |  |  |
| OULD |  |  |  |  |
| IGHT |  |  |  |  |
| HAVE |  |  |  |  |
| HICH |  |  |  |  |
| WHIC |  |  |  |  |
| THIS |  | X |  |  |
| THIN | X | X |  |  |
<!--- END RECEIVE ORGTBL quadrigrams -->

<!---
#+ORGTBL: SEND quadrigrams orgtbl-to-gfm
| Quadrigram | Keymacs | Norman | Colemak | Dvorak |
|------------+---------+--------+---------+--------|
| THAT       | X       | X      |         | X      |
| THER       | X       |        |         |        |
| WITH       |         |        |         |        |
| TION       | X       | X      | X       |        |
| HERE       | X       |        |         |        |
| OULD       |         |        |         |        |
| IGHT       |         |        |         |        |
| HAVE       |         |        |         |        |
| HICH       |         |        |         |        |
| WHIC       |         |        |         |        |
| THIS       |         | X      |         |        |
| THIN       | X       | X      |         |        |
-->

In Keymacs 5/12 of the most frequent quadrigrams placed in home row
without finger movement. Other compared layouts have less
quadrigrams in home row. Only Norman has good result too.

In Keymacs most of time you will use home row of your keyboard
(carpalx simulator shows >70% of home row usage on default
corpus of English texts).

### Additional remaps

I strongly recommend remap `Control` keys in upper rows instead of
placing defaults in lower row. For example on my Lenovo I did remap to
`CapsLock` for `LCtl` and to `Enter` for `RCtl`. So they placed on
left and right side of home row now (and `Enter` was moved to original
`Ctl` keys). It depends on a keyboard model.

You would like remap `Alt` keys too because `Meta` key (that called
`Alt` on PC keyboards) is very actively used in Emacs.

### Navigation keys

Emacs by default uses holding Control and pressing `F` `B` for
navigating right-left and `P` `N` for navigating up-down.  It is easy
for remember because of mnemomic names but badly placed in
QWERTY. Keymacs places all these keys for one hand usage (under a left
hand). Statistically the most used navigation key in Emacs is moving
cursor down so it placed in home row without a finger movement (`N`).

!["Navigation keys"](keymacs-navigation-keys.png)

The block of navigation keys includes `A` and `E` that used in Emacs
for moving to the beginning or to the end of line.

Well it may look a bit alien. But it is no more alien than Vim' HJKL
:) With remapped `Ctl` keys (like described in a paragraf above) it is
comfortable with no matter which hand used for pressing `Ctl`. I
specially placed up/down arrows with horizontal shift so you can press
down arrow with index finger on home row and up arrow with middle
finger. Contrary to traditional placement of up/down arrows on
additional keyboard where you need use the same middle finger for both
keys.

For the list of the most often pressed key combinations in Emacs
I used statistics results from
[ergoemacs.org/emacs/command-frequency.html](http://ergoemacs.org/emacs/command-frequency.html).

### State of the project

This my research for the best keyboard continues for a long time. I
had tried different well known alternatives like Colemak and Workman
and after that started with my custom keyboard in 2014 (link
to [the previous effort](https://github.com/grafov/keyboard)). I am
still using it. After all it is far from finish. Though I already got
much more comfortable layout for my needs than default but it still
has a lot of drawbacks. So I can't recommend to use it yet. But I hope
my results may inspire you to find your own right path to the ideal.

Though I mostly satisfied with letters there are many place for
improvement for numbers placement and non-letter symbols. So the
layout continues to evolve.

### Carpalx results for the layout

	Keyboard effort
	------------------------------------------------------------
	k1                      0.790  78.4  78.4
	k1,k2                   0.980  18.8  97.2
	k1,k2,k3                1.008   2.8 100.0
	b                       0.336  18.6  18.6
	p                       0.672  37.3 149.9
	ph                      0.000   0.0   0.0
	pr                      0.166  24.7  24.7
	pf                      0.431  64.1  88.8
	s                       0.795  44.1 100.0
	all                     1.803 100.0 100.0

	#data effort_k1=>[0.790,78.380,78.380],
	#data effort_k12=>[0.980,18.832,97.212],
	#data effort_k123=>[1.008,2.788,100.000],
	#data effort_base=>[0.336,18.616,18.616],
	#data effort_penalty=>[0.672,37.288,149.924],
	#data effort_penalty_hand=>[0.000,0.000,0.000],
	#data effort_penalty_row=>[0.166,24.693,24.693],
	#data effort_penalty_finger=>[0.431,64.134,88.827],
	#data effort_path=>[0.795,44.096,100.000],
	#data effort_all=>[1.803,100.000,100.000],

	keyboard row frequency
	------------------------------------------------------------
	1                     1483367 16.2  16.2
	2                     6734080 73.6  89.8
	3                      933718 10.2 100.0

	#data row_data=>[qw(1 2 3)],
	#data row_frequency=>[0.162,0.736,0.102],
	#data row_cumulative=>[0.162,0.898,1.000],

	keyboard hand frequency
	------------------------------------------------------------
	0                     4634796 50.6  50.6
	1                     4516369 49.4 100.0

	#data hand_data=>[qw(0 1)],
	#data hand_frequency=>[0.506,0.494],
	#data hand_cumulative=>[0.506,1.000],

	keyboard finger frequency
	------------------------------------------------------------
	0                      539877  5.9   5.9
	1                      895424  9.8  15.7
	2                     1540730 16.8  32.5
	3                     1658765 18.1  50.6
	6                     1806945 19.7  70.4
	7                     1211914 13.2  83.6
	8                      918154 10.0  93.7
	9                      579356  6.3 100.0

## Known problems

* Layout has high rate of consecutive finger usage for index fingers.
* Navigation block need more research (all keys ←↓↑→ on one hand VS
  splitted ↓↑ on left and ←→ on right).

## Separated navigation layer

See [Control Layer](https://github.com/keyboard-ergonomics/control-layer).

## Project status after 5 years

One thing that I know today — the keyboard layout optimization is
endless process :)

I mostly satisfied with current results. In 2017 I moved to [Ergodox EZ
keyboard](http://ergodox-ez.com) and [adapted Keymacs layout to
it](https://github.com/grafov/qmk_firmware/tree/master/keyboards/ergodox_ez/keymaps/grafov). It
looks [like
this](https://configure.ergodox-ez.com/keyboard_layouts/bljxnj).

![Adaptation of Keymacs for Ergodox](keymacs-on-ergodox.png)

## License

This work dedicated to the public domain.
