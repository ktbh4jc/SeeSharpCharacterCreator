# Welcome to the See Sharp Character Creator

## What is this?  
Basically, I wanted to learn C#, and the best way to learn a language is to start a project and get it going. My project is a fairly simple Character Creator for Dungeons and Dragons 5e.

## Wow, a character creator has a lot of info if you plan to include everything. Didn't you say you were doing saomething fairly simple?
Yeah, I'm skipping some stuff. No feats, only a couple races, classes, and spells. No subclasses yet, but that is something I would like to get to.

## How are you defining different parts of a character?
For my first pass, I am going to define Characters, Races, Classes, and Spells as such:

```
Character:
	Race -> Race
	Classes -> [(Class1, Level<int>), (Class2, Level<int>)...]
	HitPoints -> int
	Spells -> [Spell1, Spell2...]
	Features -> {Name1<String>: Description1<String>, Name2<String>: Description2<String>}
	Speed -> int
	Lanuages -> {String}
	AbilityScores -> {"STR": int, "DEX": int, "CON": int, "INT": int, "WIS": int, "CHA": int}
	SpellSlots -> [int]
```

```
Race:
	Features -> {Name1<String>: Description1<String>, Name2<String>: Description2<String>}
	BaseSpeed -> int
	Size -> String
	Languages -> {String}
```

```
Class:
	ProgressionChart -> {1: [FeatureName1<String>, FeatureName2<String>, ...], 2[FeatureName3<String>, FeatureName4<String>...] ... }
	Features -> {FeatureName1<String>: Description1<String>,FeatureName2<String>: Description2<String> ...}
	HitDie-> int
	Spells -> [Spell1, Spell2...]
	SpellcastingAbility -> String
```

```
Spell:
	Level -> int # 0 meaning cantrip
	Components -> {Verbal: bool, Somatic: bool, Material: bool}
	Materials -> String
	Concentration -> Bool
	Duration -> String
	Range -> String
	Description -> String
```






