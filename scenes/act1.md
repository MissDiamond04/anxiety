# act1

```
SceneSetup.act1();
```

(...300)

n: EN DIT IS HAAR ANST

n: _JIJ_ BENT DE ANGST

{{if window.localStorage.continueChapter=="replay"}}
(#act1_replay)
{{/if}}

{{if window.localStorage.continueChapter!="replay"}}
(#act1_normal)
{{/if}}



# act1_replay

`hong({mouth:"0_neutral", eyes:"0_neutral"})`

h: Oh hey! Zijn we hier weer?

`hong({eyes:"0_neutral"})`

n: JE BAAN IS OM JOUW MENS TE BESCHERMEN TEGEN *GEVAAR* 

`bb({eyes:"look", mouth:"small_lock"})`

n: ERGER NOG, DEZE GAME OPNIEUW SPELEN BRENGT HAAR NU IN *GEVAAR*

n: SNEL, WAARSCHUW HAAR!

```
sfx("squeak");
bb({body:"squeeze_talk"});
hong({body:"0_squeeze"});
```

b: Mens! Luister, we zijn in gevaar! De speler...

[...gaat ons weer martelen!](#act1_replay_torture)

[...kan geen ander einde vinden!](#act1_replay_alternate)

[...krijgt ludonarratieve dissonantie!](#act1_replay_dissonance)

# act1_replay_torture

```
window.HACK_REPLAY = JSON.parse(localStorage.act4);
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

{{if window.HACK_REPLAY.act1_ending=="fight"}}
b: Laat ons in een bal kruipen en huilen! 
{{/if}}

{{if window.HACK_REPLAY.act1_ending=="flight"}}
b: Gaat je telefoon kapot laten maken omdat je een paniekaanval had!
{{/if}}

{{if window.HACK_REPLAY.a2_ending=="fight"}}
b: Laat ons *NIET* de gastheer van het feest slaan! 
{{/if}}

{{if window.HACK_REPLAY.a2_ending=="flight
b: Ze laten ons de sympathieke gastheer van het anti-schurkfeest slaan! 
{{/if}}

{{if window.HACK_REPLAY.a3_ending=="jump"}}
h: Nou misschien springen we deze keer niet van het dak-
{{/if}}

{{if window.HACK_REPLAY.a3_ending=="walkaway"}}
b: ZE GAAN ONS VAN HET DAK LATEN SPRINGEN.
{{/if}}

`bb({body:"fear"});`

b: AL DEZE NIEUWE VERSCHRIKKELIJKE DINGEN GAAN MET ONS GEBEUREN, EN DAN-- 

(#act1_replay_end)


#act1_replay_alternate

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

h: Zeker, het verhaal als een *geheel* is hetzelfde, maar elk hoofdstuk heeft 2 verschillende eindes, plus al het-- 

`bb({body:"fear"});`

b: De speler zal teleurgesteld zijn, sluit deze tab, delete onze software, en dan kunnen we--

(#act1_replay_end)


# act1_replay_dissonance

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

h: Een lewd-wat zei je nou?

`bb({eyes:"normal"});`

b: De verhaallijn ging over hoe je kon *KIEZEN* om een gezonde samenwerking op te bouwen met je angst,

`bb({eyes:"normal_right"});`

b: Maar het opnieuw spelen van het spel geeft hetzelfde verhaal, wat impliceert dat jouw *KEUZES* er niet toe doen,

`bb({eyes:"narrow_eyebrow"});`

b: Aldus een tegenstelling laten zien tussen de boodschap van het spel en de mechanica,

`bb({eyes:"fear"});`

b: Aldus de structuur van dit verhalende universum ontrafelen,

`bb({body:"fear"});`

b: En dan zullen we--

(#act1_replay_end)


# act1_replay_end

`bb({body:"panic"})`

b: DOODGAAAAAAAAAN

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.clearText();
```

(...1001)

```
bb({body:"laugh"});
hong({body:"laugh"});
Game.clearText();
sfx("laugh");
```

(...5001)

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({body:"0_sammich"});
```

h: Oke laten we weer teruggaan naar het normaal

```
Game.clearText();
```

n4: (LAAT _JOUW_ ANGST BLAH BLAH MEEST VERGELIJKBAAR ZIJN MET WAT _JOUW_ ANGST BLAH BLAH JE SNAPT HET WEL)

```
sfx("squeak");
hong({body:"0_squeeze"});
bb({body:"squeeze"});
```

(#act1_normal_choice)



# act1_normal

`hong({mouth:"0_neutral", eyes:"0_annoyed"})`

h: Oh goed, mijn wolf is terug. Faaaantastisch.

`hong({eyes:"0_neutral"})`

n: JE BAAN IS OM JOUW MENS TE BESCHERMEN TEGEN *GEVAAR* 

`bb({eyes:"look", mouth:"small_lock"})`

n: ERGER NOG, DAT BROODJE BRENGT HAAR NU IN *GEVAAR*

n: SNEL, WAARSCHUW HAAR!

```
sfx("squeak");
bb({body:"squeeze_talk"});
hong({body:"0_squeeze"});
```

b: Mens! Luister, we zijn in gevaar! Het gevaar is...

`bb({body:"squeeze"})`

n4: (TIJD OM TE SPELEN! KIES WAT HET MEEST VERGELIJKBAAR IS MET WAT _JOUW_ ANGST JE VERTELT)

(#act1_normal_choice)

# act1_normal_choice

[We eten alleen voor de lunch! Alweer!](#act1a_alone) `bb({body:"squeeze_talk"})`

[We zijn niet productief tijdens het eten!](#act1a_productive) `bb({body:"squeeze_talk"})`

[Dat witte brood is slecht voor ons!](#act1a_bread) `bb({body:"squeeze_talk"})`

# act1a_alone

```
bb({body:"normal", mouth:"small", eyes:"narrow"});
hong({body:"0_sammich"});
```

b: Weet je niet dat eenzaamheid leidt tot vroegtijdige dood, en net zo erg is als 15 sigaretten per dag roken?

`Game.OVERRIDE_TEXT_SPEED = 2;`

`bb({mouth:"normal", eyes:"normal_right"})`

b: (Holt-Lunstad 2010, PLoS Medicine)

`hong({eyes:"0_annoyed"})`

h: Um, bedankt voor dat leuke feitje maar-- 

`Game.OVERRIDE_TEXT_SPEED = 2;`

`bb({body:"fear", mouth:"normal", eyes:"fear"})`

b: Wat betekent als we niet *nu* met iemand anders chillen dat we--

`bb({body:"panic"})`

b: DOODGAAAAAAAAN!

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "alone");
publish("hp_show");
```

(...2500)

`_.fifteencigs = true`

n: JE GEBRUIKTE *ANGST OM ONGELIEFD TE ZIJN*

(#act1b)

# act1a_productive

```
bb({body:"normal", mouth:"small", eyes:"normal"});
hong({body:"0_sammich"});
```

b: Pak je laptop en ga nu werken! 

`hong({eyes:"0_annoyed"})`

h: Um, ik wil liever geen kruimels op mijn keyboa--

```
bb({mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Als we niet bijdragen aan het lichaam van de samenleving, zijn we een samenleving-parasiet!

b: De samenleving-lichaam gaat naar de samenleving-arts voor medicatie om hun samenleving-parasieten te doden, dan gaan we--

```
bb({body:"panic", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: DOOOOOOOOOOOD

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "bad");
publish("hp_show");
```

(...2500)

`_.parasite = true`

n: JE GEBRUIKTE *ANGST OM EEN SLECHTE PERSOON TE ZIJN*

(#act1b)

# act1a_bread

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich", eyes:"0_annoyed"});
```

h: Zijn die onderzoeken herhaa--

```
bb({body:"fear", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Bewerkt tarwe zal onze bloedsuikerspiegel doen stijgen, dan moeten ze al onze ledematen amputeren en dan gaan we-
   
`bb({body:"panic"})`

b: DOOOOOOOOOOOOOOOOOD

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "harm");
publish("hp_show");
```

(...2500)

`_.whitebread = true`

n: JE GEBRUIKTE *ANGST OM GESCHAAD TE WORDEN*

(#act1b)

# act1b

n: HET IS SUPER EFFECTIEF

`bb({mouth:"smile", eyes:"smile"});`

b: Zie je, mens? Ik ben je trouwe wachtwolf!

`bb({body:"pride_talk"});`

b: Vertrouw je gevoelens! Die zijn altijd geldig!

`bb({body:"pride"});`

n: MAAK DE ENERGIEBALK VAN UW MENS NUL

n: OM HUN FYSIEKE + SOCIALE + MORELE BEHOEFTEN TE BESCHERMEN, KAN JE GEBRUIKEN:

n: ANGST OM *GESCHAAD TE WORDEN* #harm#

n: ANGST OM *ONGELIEFD TE ZIJN* #alone#

n: EN ANGST OM *EEN SLECHT PERSOON TE ZIJN* #bad#

`Game.OVERRIDE_TEXT_SPEED = 1.25;`

n4: (PRO-TIP: KIES DE KEUZES DIE PERSOONLIJK JE DIEPSTE, DONKERSTE ANGST RAKEN!~)

h: ...

```
hong({body:"putaway"});
sfx("rustle");
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

(...1000)

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

h: weet je wat misschien moet ik even mijn phone checken. 

```
sfx("rustle2");
hong({body:"phone1", mouth:"neutral", eyes:"neutral"})
```

n: BESCHERM UW MENS

n: TEGEN MENSEN. TEGEN DE WERELD. TEGEN HAARZELF.

n: VEEL SUCCES

(...500)

`Game.clearText()`

(...500)

(#act1c)

# act1c

`music('battle', {volume:0.5})`

n: RONDE EEN: *VECHT!*

`bb({body:"normal", mouth:"normal", eyes:"normal"});`

h: Huh. Facebook zegt dat er dit weekend een feestje is.

`bb({eyes:"uncertain"});`

b: Gooit die rare gast niet *elk* weekend een feestje? 

`bb({eyes:"uncertain_right"});`

b: Welke innerlijke leegte proberen ze te vullen? Ze moeten diep in de war zijn van binnen!

`hong({eyes:"surprise"});`

h: En, ik heb een uitnodiging?

`bb({eyes:"fear", mouth:"normal"});`

b: Nou dan!

[Zeg ja, anders gaan we dood aan eenzaamheid!](#act1c_loner)

[Zeg nee, het is vol met giftige drugs!](#act1c_drugs)

[Negeer het, we verpesten feestjes toch.](#act1c_sad)

# act1c_loner

{{if _.fifteencigs}}
b: Vijftien sigaretten per dag, mens! Vijftien!
{{/if}}

{{if !_.fifteencigs}}
`Game.OVERRIDE_TEXT_SPEED = 1.5;`
{{/if}}

{{if !_.fifteencigs}}
b: Dan komt er niemand op onze begrafenis, ze zullen onze as in de oceaan dumpen, we worden opgegeten door een walvis,
{{/if}}

{{if !_.fifteencigs}}
b: en dan worden we WALVISPOEP!
{{/if}}

{{if !_.fifteencigs}} `_.whalepoop = true` {{/if}}

(...500)

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`bb({eyes:"normal"});`

{{if !_.fifteencigs}}
b: Dus laten we naar het feestje gaan!
{{/if}}

{{if _.parasite}}
b: Maar breng de laptop mee zodat we kunnen werken, en geen parasiet in de samenleving worden.
{{/if}}

{{if _.whitebread}}
b: Zolang ze maar geen WIT BROOD serveren
{{/if}}

`hong({mouth:"anger", eyes:"anger"});`

h: OKE. Als het je laat zwijgen, prima.

h: Ik ga ja zeggen.

{{if _.whalepoop}}
b: Walvispoep, mens. Walvis poep.
{{/if}}

`_.partyinvite="yes"`

(#act1d)

# act1c_drugs

`bb({mouth:"small", eyes:"fear"});`

{{if _.whitebread}}
b: of nog slechter... WIT BROOD
{{/if}}

{{if _.whitebread}}
`Game.OVERRIDE_TEXT_SPEED = 1.5;`
{{/if}}

{{if _.whitebread}}
b: We zullen op zoveel meth en wit brood overdoseren dat ze ons dikke lijk niet in de crematieovens kunnen stoppen!
{{/if}}

{{if !_.whitebread}}
b: We zullen aan zoveel drugs overdoseren dat de begrafenisondernemer zal afvragen hoe ons lichaam *al* voorgebalsemd was!
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

{{if _.parasite}}
b: Trouwens, we kunnen niet feesten, we moeten werken of we zijn een vreselijke samenleving-parasiet!
{{/if}}

`hong({mouth:"anger", eyes:"anger"});`

h: OKE. Als het je laat zwijgen, prima.

h: Ik zeg wel nee.

`_.partyinvite="no"`

(#act1d)

# act1c_sad

`bb({eyes:"uncertain_right", mouth:"normal"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

{{if _.fifteencigs}}
b: Het enige wat we doen is in een hoek huilen over hoe eenzaamheid net zo dodelijk is als 15 sigaretten per dag.
{{/if}}

{{if _.parasite}}
b: Het enige wat we op feestjes doen is ons zorgen maken over hoe we eigenlijk productief zouden moeten zijn.
{{/if}}

{{if _.whitebread}}
b: Het enige dat we doen is ons zorgen maken over hoe de ongezonde voedselopties ons zullen doden.
{{/if}}

```
bb({mouth:"normal", eyes:"normal"});
hong({mouth:"neutral", eyes:"lookaway"});
```

h: wauw vraag me af waarom.

`hong({eyes:"neutral"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

b: Dus als we gaan zullen we ze een slecht gevoel geven, maar als we niet gaan, zullen we ze ook een slecht gevoel geven!

`bb({body:"fear", eyes:"fear"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

b: ALLES WAT WIJ DOEN IS MENSEN ZICH ROT LATEN VOELEN, DUS MOETEN WIJ ONS OOK ZO VOELEN

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

`hong({mouth:"anger", eyes:"anger"});`

h: Ugh. Als het je laat zwijgen, prima.

h: Ik negeer de uitnodiging.

`_.partyinvite="ignore"`

(#act1d)

# act1d

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"neutral", eyes:"annoyed"});
```

h: Nou ja. Facebook is te veel. Ik heb iets rustigers nodig, dat minder angst veroorzaakt.

`hong({eyes:"neutral"});`

h: Wat is nieuw op Twitter?

`bb({eyes:"look"});`

[Oh nee, kijk naar dat erge nieuwsbericht!](#act1d_news)

[Oh nee, gaat die tweet stiekem over *ons?*](#act1d_subtweet)

[Hey, een GIF van een kat die melk drinkt](#act1d_milk)


# act1d_news

```
bb({eyes:"pained1"});
music(null, {fade:2});
```

b: Wow, lijkt net of de planeet brandt, nietwaar?

```
bb({eyes:"pained2"});
hong({mouth:"sad", eyes:"sad"});
```

b: Het voelt alsof het allemaal eindigt, alsof alles aan het sterven is en wij kunnen er niets aan doen.

```
Game.OVERRIDE_TEXT_SPEED = 0.5;
bb({mouth:"shut"});
```

b: ...

`bb({mouth:"smile", eyes:"smile"});`

b: Laten we dat verhaal retweeten!

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

`_.badnews=true`

```
music('battle', {volume:0.5});
hong({mouth:"anger", eyes:"anger"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Oke ik retweet het wel maar wees dan stil!

`hong({mouth:"neutral", eyes:"annoyed"});`

h: Laat maar, laten we naar Snapchat gaan.

(#act1e)


# act1d_subtweet

`bb({eyes:"fear"});`

b: Het is een subtweet! Een stiekeme, stiekeme subtweet!

`hong({eyes:"annoyed"});`

h: Nee dat is het niet?

`bb({eyes:"narrow", mouth:"small"});`

b: maar wat als ze allemaal achter onze rug praten?

h: Ze zijn nie--

`bb({body:"fear", eyes:"fear", mouth:"normal"});`

b: VOOR ONZE RUG

`hong({eyes:"sad", mouth:"sad"});`

h: Ik de--

`bb({eyes:"narrow", mouth:"small"});`

b: maar *wat als*

h: N--

`bb({eyes:"narrow_eyebrow"});`

b: *wat als*

```
Game.OVERRIDE_TEXT_SPEED = 0.5;
hong({mouth:"shut"});
```

h: ...

(...1000)

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`_.subtweet=true`

```
hong({mouth:"anger", eyes:"annoyed"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: o-KAY, ik ga nu naar Snapchat.

(#act1e)

# act1d_milk

`hong({mouth:"smile", eyes:"neutral"});`

h: Heh ja dat is schattig, net geretweet, ik d--

```
hong({mouth:"shock", eyes:"shock"});
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.8;
```

b: KATTEN KUNNEN MELK NIET VERTEREN EN WIJ ZIJN VRESELIJKE MENSEN OMDAT WE GENIETEN VAN DIERENMISHANDELING

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
attack("18p", "bad");
```

(...2500)


`_.catmilk=true`

```
hong({mouth:"anger", eyes:"annoyed"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: o-KAY, ik ga nu naar Snapchat.

(#act1e)

# act1e

`hong({mouth:"neutral", eyes:"neutral"});`

h: Huh, foto's van gisteravond. Dus *dat* is hoe die wekelijkse feestjes zijn.

{{if _.partyinvite=="yes"}} (#act1e_said_yes) {{/if}}

{{if _.partyinvite=="no"}} (#act1e_said_no) {{/if}}

{{if _.partyinvite=="ignore"}} (#act1e_said_ignore) {{/if}}

# act1e_said_yes

`hong({mouth:"sad", eyes:"annoyed"});`

h: Oof, ziet er veel te druk uit voor mijn angst.

h: Misschien had ik geen ja moeten zeggen tegen de uitnodiging?

```
hong({mouth:"neutral", eyes:"neutral"});
bb({mouth:"normal", eyes:"normal"});
```

[Ons antwoord wijzigen? Als een eikel ?!](#act1e_yes_dontchange)

[Verander ons antwoord! Het is te druk!](#act1e_yes_changetono)

{{if _.subtweet}}
[Ja, ze waren ons sowieso aan het subtweeten.](#act1e_ignore_subtweet)
{{/if}}

{{if _.badnews}}
[Wacht, we hebben geretweet zonder de feiten te controleren.](#act1e_ignore_factcheck)
{{/if}}

{{if (!_.subtweet && !_.badnews)}}
[Weet je dat je echt een slechte houding hebt?](#act1e_ignore_posture)
{{/if}}

# act1e_yes_dontchange

```
bb({eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Ze rekenden op ons om te komen en nu beschamen we hun vertrouwen? Wil je alleen sterven?!

{{if _.fifteencigs}}
b: VIJFTIEN. SIGARETTEN.
{{/if}}

{{if _.whalepoop}}
b: WALVIS. POEP.
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

```
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Shut up shut up ik ga wel oke!

(#act1f)

# act1e_yes_changetono

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Weet je niets van menselijke stampedes?

```
bb({body:"fear", mouth:"small", eyes:"narrow"});
hong({eyes:"sad", mouth:"sad"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Eens stond een club in Rhode Island in brand en de paniek zorgde ervoor dat mensen de uitgangen blokkeerden, waardoor 100 mensen verbrandden-

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({mouth:"shock"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: WIL JE DAT DAT BIJ ONS GEBEURT-

```
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 2.5;
```

b: ZEG NEE ZEG NEE ZEG NEE ZEG NEE ZEG NEE ZEG NEE ZEG NEE ZEG N-


```
bb({body:"normal", eyes:"fear", mouth:"normal"});
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

```
hong({eyes:"anger", mouth:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Shut up shut up ik verander mijn antwoord wel naar nee!

(#act1f)

# act1e_said_no

`hong({mouth:"sad", eyes:"sad"});`

h: Hm... dat ziet er leuk uit.

h: Misschien moest ik geen nee zeggen tegen de uitnodiging?

`bb({mouth:"normal", eyes:"normal"});`

[Ons antwoord veranderen? Als een eikel?!](#act1e_no_dontchange)

[Verander ons antwoord! Ga niet alleen dood!](#act1e_no_changetoyes)

{{if _.subtweet}}
[Ze waren ons sowieso aan het subtweeten.](#act1e_ignore_subtweet)
{{/if}}

{{if _.badnews}}
[Wacht, we hebben geretweet zonder de feiten te controleren.](#act1e_ignore_factcheck)
{{/if}}

{{if (!_.subtweet && !_.badnews)}}
[Wist je dat je een hele slechte houding hebt?](#act1e_ignore_posture)
{{/if}}

# act1e_no_dontchange

`bb({eyes:"anger"})`

b: Iedereen rekende op ons!

b: ...om ze met rust te laten en een leuk feestje te geven zonder een vreselijke {{if _.whitebread}}wit-brood-eter{{/if}} engerd zoals jij--


```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

```
bb({body:"normal", eyes:"uncertain", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Shut up shut up ik hou het wel als nee!

(#act1f)

# act1e_no_changetoyes

```
bb({body:"fear", eyes:"fear", mouth:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Chronische eenzaamheid verhoogt onze cortisolspiegel en verhoogt het risico op hart- en vaatziekten en beroertes!

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

{{if _.fifteencigs}}
b: VIJFTIEN. SIGARETTEN.
{{/if}}

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Shut up shut up ik verander mijn antwoord wel naar ja!

(#act1f)

# act1e_ignore_subtweet

```
bb({eyes:"fear", mouth:"small"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Al onze problematische tweets zijn teruggekomen!

```
bb({body:"fear", eyes:"fear", mouth:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.7;
```

b: We worden gebeld en geannuleerd en met een touw te paard over de informatiesnelweg gesleept!

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Waarom ben je zo?!

(#act1f)

# act1e_ignore_factcheck

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: We verspreiden verkeerde informatie! We vernietigen het vertrouwen in een vrije pers!

```
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Wij zijn de reden dat het fascisme zal ontstaan uit het puin van de democratie!

```
bb({body:"normal", eyes:"anger"});
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

```
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
_.factcheck = true;
```

h: Waarom ben je zo?!

(#act1f)

# act1e_ignore_posture

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Wil je een krakeling voor een ruggengraat hebben?! Stop met over je scherm te hangen!

```
bb({body:"meta"});
```

b: En ik heb het ook tegen jou.

```
bb({body:"normal", mouth:"normal"});
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Waarom ben je zo?!

(#act1f)

# act1e_said_ignore

`hong({mouth:"sad", eyes:"sad"})

h: Hm... that looks really fun.

h: Misschien moest ik de uitnodiging niet negeren?

`bb({mouth:"normal", eyes:"normal"});`

[Blijf negeren, we zijn nog steeds feest verpesters.](#act1e_ignore_continue)

[Weet je wat, zeg ja.](#act1e_ignore_changetoyes)

[Weet je wat, zeg nee.](#act1e_ignore_changetono)

# act1e_ignore_continue

`hong({eyes:"annoyed"});`

h: Het is nogal onbeleefd om ze te blijven negeren, niet?

`bb({eyes:"normal_right"});`

b: Tsja andere mensen negeren steeds *ons*, dus

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`bb({eyes:"normal"});`

b: dus nu staan we weer gelijk.

(#act1f)

# act1e_ignore_changetoyes

`hong({eyes:"surprise", mouth:"smile"});`

h: Je... laat me plezier hebben?

b: Nou ja, ik bedoel, eenzaamheid *kan* ons vermoorden.

`hong({eyes:"neutral", mouth:"neutral"});`

(#act1e_no_changetoyes)

# act1e_ignore_changetono

`bb({eyes:"narrow"});`

b: Het is te druk. Menigten zijn gevaarlijk.

(#act1e_yes_changetono)


# act1f

```
hong({mouth:"neutral", eyes:"neutral"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: Wat dan ook. Nieuwe Tinder notificatie.

`bb({eyes:"uncertain"})`

b: Wat, die hookup app?

`hong({eyes:"annoyed"})`

h: Het is geen hookup app, 't is gewoon een manier om nieuwe mense--

`bb({eyes:"narrow"})`

b: Het is een hookup app.

```
hong({eyes:"surprise", mouth:"smile"});
bb({eyes:"normal"});
```

h: Oh, ik heb een match! Die ziet er cute uit!

```
bb({eyes:"narrow_eyebrow"});
hong({eyes:"sad", mouth:"anger"})
```

h: Verpest dit alsjeblieft niet voor m-- 

```
bb({body:"panic"});
Game.OVERRIDE_TEXT_SPEED = 2.0;
```

b: GEVAAR GEVAAR GEVAAR GEVAAR GEVAAR

`bb({body:"fear", eyes:"fear", mouth:"normal"})`

[We worden *gebruikt* door andere mensen.](#act1f_used_by_others)

[We *gebruiken* andere mensen.](#act1f_using_others)

[JOUW MATCH IS EEN SERIEMOORDENAAR](#act1f_killer)

# act1f_used_by_others

`bb({body:"point_crotch", eyes:"normal", mouth:"normal"})`

b: Willekeurige hookups kunnen het gat daar beneden misschien vullen,

b: maar ze kunnen het gat nooit vullen...

`bb({body:"point_heart", eyes:"pretty", mouth:"small"})`

b: *hierbinnen*.

(...1000)

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Het punt is WE ZULLEN ALLEEN DOODGAAN

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`_.hookuphole=true`

(#act1g)

# act1f_using_others

`bb({eyes:"narrow", mouth:"small"})`

b: Denk je dat de geslachtsdelen van andere mensen Pokémons zijn die wij kunnen verzamelen?

```
bb({body:"sing", eyes:"pretty", mouth:"shut"});
music("pokemon");
Game.clearText();
Game.FORCE_CANT_SKIP = true;
```

```
Game.FORCE_TEXT_DURATION = 1000;
Game.FORCE_NO_VOICE = true;
```

b: ♫ (pokemon theme song)-

(...5600)

```
bb({mouth:"normal"});
Game.FORCE_TEXT_DURATION = 2400;
```

b: ♫ Ik wil de ^slet^ter-igste zijn-

(...500)

```
bb({eyes:"narrow", mouth:"small"});
Game.FORCE_TEXT_DURATION = 2100;
```

b: ♫ Zoals niemand ooit geweest is-

(...1500)

```
bb({eyes:"pretty"});
Game.FORCE_TEXT_DURATION = 2300;
```

b: ♫ Dijen en ^ass^, wellustige borsten

(...500)

```
bb({eyes:"fear", mouth:"normal"});
Game.FORCE_TEXT_DURATION = 2000;
```

b: ♫ met zweterige ^dick^ en ballen!-

(...1000)

```
bb({eyes:"smile", mouth:"smile"});
Game.FORCE_TEXT_DURATION = 1000;
```

b: ♫ PERVY-MON! MOET ZE ALLE-

```
Game.FORCE_CANT_SKIP = false;
Game.clearText();
music(false);
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Het punt is dat we een manipulatieve engerd zijn.

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

`_.pokemon=true`

(#act1g)

# act1f_killer

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

{{if _.whitebread}}
b: Ze sluiten je op in een put en voeren je witbrood om je vet te maken, zodat ze je huid als een pak kunnen dragen!
{{/if}}

{{if _.parasite}}
b: Ze zullen je afknallen met een pomodoro-timer en zeggen "JE MOET PRODUCTIEVER ZIJN JIJ PARASIET"
{{/if}}

{{if !_.whitebread && !_.parasite}}
b: Ze scheuren je vlees tot bloederige confetti, veranderen je ingewanden in streamers en mengen je bloed in een punch bowl!
{{/if}}

{{if !_.whitebread && !_.parasite}}
b: Hoe is DAT voor een feestuitnodiging?!
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

`_.serialkiller=true`

(#act1g)

# act1g

```
bb({body:"normal", mouth:"normal", eyes:"look"});
hong({body:"2_tired"});
Game.OVERRIDE_TEXT_SPEED = 0.5;
music(false);
```

h: ...

(...500)

h: ik wordt zo moe van dit spel.

(...700)

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

h:
{{if _.fifteencigs}}"loneliness will kill us"... {{/if}}
{{if _.parasite}}"we're a society-parasite"... {{/if}}
{{if _.whitebread}}"don't eat that, it'll kill us"... {{/if}}
{{if _.subtweet}}"they're talking behind our back"... {{/if}}
{{if _.badnews}}"the world is burning"... {{/if}}
{{if _.hookuphole}}"we'll die alone"... {{/if}}
{{if _.serialkiller}}"they're a serial killer"... {{/if}}
{{if _.catmilk}}"cats can't digest milk"... {{/if}}
{{if _.pokemon}}a ^crappy^ parody song... {{/if}}

h: ik wil gewoon mijn leven leiden.

h: ik wil gewoon vrij zijn van al mijn pijn.

`bb({eyes:"look_sad"});`

b: Hey... mens...

`Game.OVERRIDE_TEXT_SPEED = 0.5;`

b: Het komt wel weer goed.

(...600)

`bb({body:"point_heart", eyes:"look_sad_smile", mouth:"smile"});`

b: Als je trouwe waak-wolf zal ik altijd op gevaar letten en mijn best doen om je te beschermen.

`bb({body:"normal", eyes:"look_sad", mouth:"smile"});`

b: Beloofd.

(...600)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({body:"phone1", eyes:"neutral", mouth:"neutral"});
```

h: Laatste app. Instagram. Wat heb jij te bieden?

`hong({eyes:"sad"});`

h: Het zijn... meer feest foto's.

`hong({mouth:"sad"});`

h: Iedereen ziet er zo blij uit. Vrij van zorgen. Vrij van angst.

`hong({mouth:"anger"});`

h: Waarom kan ik niet zijn zoals zij? Waarom kan ik niet gewoon *normaal* zijn? 

`bb({eyes:"normal_right"});`

b: Over feestjes gesproken, over die uitnodiging voor dit weekend. Hier is mijn LAATSTE beslissing:

`bb({eyes:"normal"});`

[We moeten gaan.](#act1g_go) `Game.OVERRIDE_CHOICE_LINE=true`

[We moeten niet gaan.](#act1g_dont) `Game.OVERRIDE_CHOICE_LINE=true`

# act1g_go

`_.act1g = "go"`

(#act1h)

# act1g_dont

`_.act1g = "dont"`

(#act1h)

# act1h

b: We moe--

```
bb({eyes:"wat", mouth:"small"});
hong({body:"2_fuck"});
```

h: *^FUCK^.*

`hong({body:"2_you"});`

h: JOU.

(...500)

b: w

(...1500)

`bb({eyes:"wat_2"});`

b: wa?

`hong({body:"phone1", eyes:"anger", mouth:"anger"});`

h: Ik ga JA zeggen tegen dat feest,

{{if _.act1g=="go"}}
h: NIET omdat jij dat wilt, maar omdat *ik* dat wil.
{{/if}}

{{if _.act1g=="dont"}}
h: Juist OMDAT je dat niet wilt.
{{/if}}

```
hong({body:"putaway"});
sfx("rustle");
```

h: Je hebt GEEN controle over mij.

```
sfx("rustle2");
hong({body:"0_sammich", eyes:"0_annoyed", mouth:"0_neutral"});
```

h: Excuseer me nu terwijl ik deze heerlijke sandwich eet in ^godverdomme^ vrede.

`hong({body:"2_sammich_eat"});`

(...601)

```
sfx("sandwich");
hong({body:"2_sammich_eaten", eyes:"0_lookaway", mouth:"0_chew1"})
```

(...601)

```
bb({body:"normal", eyes:"uncertain", mouth:"shut"});
Game.OVERRIDE_TEXT_SPEED = 0.5;
```

b: ...

```
bb({eyes:"normal_right"});
Game.OVERRIDE_TEXT_SPEED = 1;
```

b: ...

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 4;
```

b: ..................

(...500)

`bb({mouth:"normal"});`

[AHHHH WE GAAN DOOOOD](#act1h_death) `Game.OVERRIDE_CHOICE_LINE = true;`

[AHHHH IEDEREEN GAAT ONS HATEN](#act1h_loneliness) `Game.OVERRIDE_CHOICE_LINE = true;`

[AHHHH WE ZIJN VERSCHRIKKELIJKE MENSEN](#act1h_worthless) `Game.OVERRIDE_CHOICE_LINE = true;`

# act1h_death

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: AHHHH WE GAAN DOOD AAAAAAHHHHHHH

```
hong({body:"3_defeated1"});
attack("100p", "harm");
```

(...2500)

(#act1i)

# act1h_loneliness

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: AHHHH IEDEREEN HAAT ONS AAAAHHHHH

```
hong({body:"3_defeated1"});
attack("100p", "alone");
```

(...2500)

(#act1i)

# act1h_worthless

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: AHHH WE ZIJN VERSCHRIKKELIJKE MENSEN AAAHHHH

```
hong({body:"3_defeated1"});
attack("100p", "bad");
```

(...2500)

(#act1i)

# act1i

```
bb({mouth:"smile_lock", eyes:"smile", body:"normal"});
music('battle', {volume:0.5});
```

n: GEFELICITEERD

(...500)

n: JE HEBT MET SUCCES DE FYSIEKE + SOCIALE + MORELE BEHOEFTEN VAN JE MENS BESCHERMD

n: KIJK EENS HOE DANKBAAR ZE IS!

(...500)

n: NU HAAR ENERGIE NUL IS, KAN JE HAAR ACTIES DIRECT CONTROLEREN

`bb({mouth:"smile", eyes:"normal"});`

n: KIES JE EIND MOVE

`bb({mouth:"small_lock", eyes:"fear"});`

n: *MAAH HAAR AF*

[{VECHT: Straf je stressvolle telefoon!}](#act1i_phone) `Game.OVERRIDE_CHOICE_LINE=true`

[{VLUCHT: Kruip in een bal en huil!}](#act1i_cry) `Game.OVERRIDE_CHOICE_LINE=true`

# act1i_phone

`bb({mouth:"normal", eyes:"narrow"})`

b: Je telefoon gaf je een paniekaanval!

`bb({eyes:"anger"})`

b: Zuckerberg en Co kapen jouw geestelijke gezondheid voor geld!

```
bb({body:"fear", eyes:"fear"});
hong({body:"3_defeated2"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Straf je telefoon! Vernietig het! Dood het!

```
Game.OVERRIDE_TEXT_SPEED = 2.5;
bb({body:"flail"});
hong({body:"3_defeated3"});
_.act1_ending = "fight";
```

b: DOOD HET DOOD HET DOOD HET DOOD HET DOOD HET DOOD HET DOOD HET DOOD HET DOOD HET DOOD HET DOOD HET DOOD HET DOOD HET DOOD HE-

(#act1j)

# act1i_cry

`bb({eyes:"fear", mouth:"normal"})`

b: De hele wereld is gevuld met gevaar!

```
bb({body:"fear"});
hong({body:"3_defeated2"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Doe net zoals het gordeldier! Kruip in een bal voor zelfverdediging!

```
Game.OVERRIDE_TEXT_SPEED = 2.5;
bb({body:"flail"});
hong({body:"3_defeated3"});
_.act1_ending = "flight";
```

b: KRUIP IN EEN BAL EN HUIL KRUIP IN EEN BAL EN HUIL KRUIP IN EEN BAL EN HUIL KRUIP I-

(#act1j)

# act1j

`SceneSetup.act1_outro()`
