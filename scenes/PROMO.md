# intro

`SceneSetup.intro();`

# intro-play-button

(...51)

[SPEEL!](#intro-start) `publish("intro-to-game-1"); Game.OVERRIDE_CHOICE_LINE=true;`

# intro-start

(...500)

`clearText()`

n3:  Voordat we beginnen, hoe zou *jij* willen lezen?

`publish("show_options_bottom")`

# intro-start-2

n3: Laten we nu beginnen...

```
publish("hide_tabs");
clearText();
```

(...1000)

`publish("intro-to-game-2")`

n2: DIT IS EEN MENS

(...600)

`clearText()`

(...300)

`publish("intro-to-game-3")`

# act1

```
SceneSetup.act1();
publish("hide_tabs");
music('battle', {volume:0.5});
```

(...300)

n: EN DIT IS HAAR ANST

n: _JIJ_ BENT DE ANGST

(#act1_normal)


# act1_normal

```
hong({body:"putaway"});
sfx("rustle");
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Nope. Nee, ik luister niet. Moet m'n phone checken.

```
sfx("rustle2");
hong({body:"phone1", mouth:"neutral", eyes:"neutral"})
```

n: JE DOEL IS OM JOUW MENS TE BESCHERMEN TEGEN *GEVAAR*

`bb({eyes:"look", mouth:"small_lock", body:"fear"})`

b: Nee! Je scrollt je leven weg op Twitter! Alweer! 

```
bb({eyes:"normal", mouth:"normal", body:"normal"});
hong({eyes:"annoyed"});
```

h: Ja ik vraag me af waarom ik niet vaker naar mijn gedachtes luister. 

`hong({eyes:"neutral"});`

n: SNEL, WAARSCHUW HAAR VOOR *GEVAAR!*

```
bb({eyes:"look"});
```

[Oh nee, kijk naar dat verschrikkelijke nieuwsbericht!](#act1d_news)

[Oh nee, gaat die tweet stiekem over *ons?*](#act1d_subtweet)

[Hey, een GIF van een kat die melk drinkt](#act1d_milk)

# act1d_milk

`hong({mouth:"smile", eyes:"surprise"});`

h: Ha ja dat is schattig, ik--

```
hong({mouth:"shock", eyes:"shock"});
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.8;
```

b: MELK IS SLECHT VOOR KATTEN EN WE ZIJN SLECHTE MENSEN OMDAT WE DIT LEUK VINDEN

(...200)

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
attack("20p", "bad");
publish("hp_show");
```



