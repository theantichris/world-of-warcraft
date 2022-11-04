# Macros

## General

### Cursor

```
#showtooltip Spell
/cast [mod:shift][@cursor] Spell; [nomod][@player] Spell
```

### Focus

```
/focus [nomod]
/focus [mod: alt, @mouseover]
/clearfocus [mod: shift]
```

### Mouseover

```
#showtooltip Spell
/cast [@mouseover,exists,nodead,help,][exists,nodead,help][@player] Spell
```

### Revive

```
#showtooltip
/console autounshift 0
/cast [@mouseover,exists,help][@target] Revive
/console autounshift 1
/use 3
```

### Trinkets

```
#showtooltip
/use 13
/use 14
```

## Death Knight

### Amry of the Dead

```
/script PlaySoundFile("Sound\\Creature\\HeadlessHorseman\\Horseman_Special_01.wav")
/cast Army of the Dead
```

### Death Grip

```
/script PlaySoundFile("Sound\\Creature\\HeadlessHorseman\\Horseman_Beckon_01.wav&qu ot;)
/cast Death Grip
```

### Lichborne

```
#showtooltip
/cast [nomod] Lichborne
/cast [nomod, @player] Death Coil
/cast [mod:alt, @pet] Death Coil
```

### Raise Dead

```
#showtooltip
/use [nopet] Raise Dead; Dark Transformation
```

## Druid

### Dash/Stampeding Roar

```
#showtooltip Dash
/cast [mod:shift] Stampeding Roar; [nomod] Dash; [nomod] Tigers Dash
```

### Forms

```
#showtooltip Bear Form
/cast [noform:1] Bear Form
```

```
#showtooltip Cat Form
/cast [noform:2] Cat Form
```

```
#showtooltip Travel Form
/cast [noform:3] Travel Form
```

```
#showtooltip Moonkin Form
/cast [noform:4] Moonkin Form
```

```
#showtooltip Treant Form
/cast [noform:5] Treant Form
```

```
#showtooltip Incarnation: Tree of Life
/cast !Incarnation: Tree of Life
```

### Form Progress

```
/run local q,x,_,a,b = GetAchievementCriteriaInfo,0 for i=1,11 do _,_,_,a,b = q(11152,i) x=a end local _,_,_,c,d = q(11153,1) local _,_,_,e,f = q(11154,1) print("Dungeons: "..x.."/"..b) print("WQs: "..c.."/"..d) print("Kills: "..e.."/"..f)
```

### Specs

```
#showtooltip Cat Form
/run SetSpecialization(GetSpecialization()==2 and 2 or 2)
```

```
#showtooltip Bear Form
/run SetSpecialization(GetSpecialization()==3 and 3 or 3)
```

```
#showtooltip Moonkin Form
/run SetSpecialization(GetSpecialization()==1 and 1 or 1)
```

```
#showtooltip Treant Form
/run SetSpecialization(GetSpecialization()==4 and 4 or 4)
```

### Regrowth

```
#showtooltip Regrowth
/console autounshift 0
/cast [@mouseover,exists,nodead,help,][exists,nodead,help][@player] Regrowth
/console autounshift 1
/use 3
```

### Skull Bash

```
#showtooltip Skull Bash
/stopcasting
/cast [noform:2,noform:1] Cat Form
/cast [@focus,exists][@target] Skull Bash;
```

### Soothe

```
#showtooltip Soothe
/stopcasting
/cast [@focus,exists][@target] Soothe
```

### Travel Form

```
#showtooltip
/cast [indoors] [combat] Cat Form;  [outdoors] Travel Form
```

```
#showtooltip Travel Form
/cast [mod:shift]Grand Expedition Yak;[mod:ctrl]Sandstone Drake;[mountable,group,nomod,noflyable,outdoors]Mount Form);[outdoors,nomod]Travel Form;[indoors,nomod]Cat Form
```
