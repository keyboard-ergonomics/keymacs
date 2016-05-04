# Keymacs — the keyboard layout for Emacs users

## Project targets

* Fix QWERTY problems (apply solutions from well known alternative layouts)
* Keep keys for general Emacs combos in convenient places

## Introduction into QWERTY keyboard layout problems

Like in many other alternative layouts first purpose of this project is
fix QWERTY problems. Second purpose is to be compatible with most typical
GNU/Emacs keybindings.

An usable keyboard layout for all purposes is a mythical idea similar
to idea of an universal programming language. A degree of usability
always depends on UI of applications you used. Different apps have
different frequency of key combinations and provide different hotkeys.
Human languages beside English increase complexity of this task
by adding own rules of keyboard usage unique per language. Also
hardware limits of common keyboards prevent to use them ergonomically
(there are a very small set of keyboards that may be called really
ergonomic).

But with all these limitations in mind it is possible to increase
usability of your keyboard for most often used by you applications
and for languages you speak. And I think resulting layout, that may be
comfortable for you will be very different from layout comfortable for me.
But... if we use nearly same set of applications and speak same language
then optimal for us layouts may be similar too. So it is main idea of this
project — *it is not possible make universal ergonomic layout for all* but
it possible make *nearly ergonomic layout* for people who used *similar tools
and speak same language*.

Yes, it possible to change keybindings in different apps to a single scheme.
But anyway adapting you keybindings will not improve QWERTY layout. So you
will choose one of alternatives like Colemak, Norman, Workman etc. But then
you will try to use it with your honest application you will find how strange
look old key combos. Especially navigation on chars/words/strings or copypasting.
For example Colemak keeps ZXCV keys in same places like in QWERTY so you will
not lost with a new layout in many GUI apps those use these keys for copy-paste
operations. But if you are Vi or Emacs user you will find a new layout very
uncomfortable for the most of typical operations because default keybindings
was oriented on QWERTY. As another example remember navigation keys in Vim:
where they placed in QWERTY and just compare with any other alternative layout.
You will find them in very inconvenient places. So if you want to use better
keyboard layout you will need change applications you use for that layout.

It main cause why I not use one of ready alternatives and research for own
solution. Because I used GNU/Emacs most of time and terminals with Emacs-like
keybindings. I also try to set Emacs keybindings in other programs where possible.
And most of time I wrote texts in English (programming languages and docs).
So with Keymacs I got layout better on many ergonomic parameters than QWERTY and
keys placement well suited for Emacs keybindings.

So it is chance that if you use Emacs and apps with Emacs-like bindings than my
keyboard layout may be good for you too :) 

![Keymacs layout](keymacs-layout.png)

## Why is it good for Emacs?

TBD

Motivation for placement all these keys on such different from QWERTY places
of cource need explanations. Explanations need significantly more time. I have
no this time currently. So it will be done later.

### Heatmaps

There are results from [patorjk.com/keyboard-layout-analyzer](http://patorjk.com/keyboard-layout-analyzer/) for
the configuration [keyboard-analyzer-config.json](keyboard-analyzer-config.json):

![Keymacs heatmap for I chapter of "Alice in Wonderland"](keymacs-heatmap-for-alice-in-wonderland.png)

Compare with QWERTY layout: 

![QWERTY heatmap for I chapter of "Alice in Wonderland"](qwerty-heatmap-for-alice-in-wonderland.png)

### Top of the most frequent letter pairs in English texts

* TH — at home row in Keymacs, not need finger movement `[+]`
* HE — at home row in Keymacs, not need finger movement `[+]`
* AN — at home row in Keymacs, not need finger movement `[+]`
* IN — at home row in Keymacs, not need finger movement `[+]`
* ER — at home row in Keymacs, not need finger movement `[+]`
* ND — at home row in Keymacs `[+/-]`
* RE — at home row in Keymacs, not need finger movement `[+]`
* ED — at home row in Keymacs `[+/-]`
* ES — at home row in Keymacs `[+/-]`
* OU — need finger movement `[-]`
* TO — at home row in Keymacs, not need finger movement `[+]`
* HA — at home row in Keymacs, not need finger movement `[+]`
* EN — at home row in Keymacs, not need finger movement `[+]`
* EA — at home row in Keymacs, not need finger movement `[+]`
* ST — at home row in Keymacs `[+/-]`
* NT — at home row in Keymacs, not need finger movement `[+]`
* ON — at home row in Keymacs, not need finger movement `[+]`
* AT — at home row in Keymacs, not need finger movement `[+]`
* HI — at home row in Keymacs, not need finger movement `[+]`
* AS — at home row in Keymacs `[+/-]`

For compare QWERTY only had *AS* pair placed at home row, but
all other pairs from the list above need move either one finger.

In Keymacs most of time you will use home row of your keyboard
(carpalx simulator shows >70% of home row usage on default
corpus of English texts).

### Navigation keys

Emacs by default uses holding Control and pressing `F` `B` for
navigating right-left and `P` `N` for navigating up-down.
It is easy for remember because of mnemomic names but not very
good placed on QWERTY. Keymacs places all these keys for one
hand usage (under a left hand). Statistically the most used
navigation key in Emacs is moving cursor down so it placed
in home row without a finger movement (`N`).

For the list of the most often pressed key combinations in Emacs
I used statistics results from
[ergoemacs.org/emacs/command-frequency.html](http://ergoemacs.org/emacs/command-frequency.html).

### State of the project

This my research for the best keyboard continues a long time (I started with my
fully custom keyboard circa 2014 and earlier I tried another layouts from the net). And
it is far from finish.
Though I already got much more comfortable layout for my needs than default but it still has
a lot of drawbacks. So I can't recommend to use it. But I hope my results may inspire you to find your own
right path to ideal.

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
* Navigation block need more tests (all keys ←↓↑→ on one hand VS splitted ↓↑ on left and ←→ on right).

## Separated navigation layer

TBD
