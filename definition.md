# Syntax Definition

```
Pattern     := { Step }
Step        := Number ":" [Rope] Action { ";" Action }
Rope        := Letter ["." Length] // needed only for the first use of the rope
Action      := Bind | Travel | Note
Bind        := BodyPart ":" Tie [Wraps] [WrapDir] [CinchOrFriction] [Angle] [Tension]
Travel      := -> Dest
Dest        := BodyPart [ "." Surface ]
Note        := "t:" Tension | "!nerve" | "!pulse" | "↔ mirror" | "[ ... ]" | "( ... ) xN"

BodyPart    := Part [ "." Side [ "." Surface ] ]
Side        := "L" | "R" | "B"      // both = symmetrical intent
Surface     := "V" | "D"

Tie          := "SC" | "DC" | "RB" | "HL" | "AL" | "CP"
Wraps       := "x" Number           // e.g., x2
WrapDir     := "cw" | "ccw"
CinchOrFriction := "CP" | "HH" | "XF" | "LK" | "SQ" | "MTR"
Angle       := "@" Clock
Clock       := "12"|"1"|"1:30"|...|"11:30"|"6"
Tension     := "soft"|"firm"|"tight"
Number      := integer
Manipulation :=
```

## Body Parts

`BodyPart    := Part [ "." Side [ "." Surface ] ]`

### Examples

* `WR.L` Left wrist
* `CHU.D` Upper chest - back

### Part

```
WR wrist
AN ankle
FA forearm
UA upper arm
EL elbow
CHU Upper Chest
CHL Lower Chest 
WA waist
HP hip
TH thigh
KN knee
CF calf
NK neck
RB ribcage
```
### Side

```
L Left
R Right
```

### Surface

```
V Ventral (Front)
D Dorsal (Back)
```

## Ties

```
SC single-column 
DC double-column 
RB rope band (simple band without a column lock)
CP cinch pass (perpendicular cinch through wraps)
AL anchor lark’s head (attach to an anchor/bight)
HL half-lashing (two bands + cinch)
```

## Friction/Locks

```
RF Reverse Friction
HH half-hitch,
XF X-friction,
LK lark’s head,
SQ square knot,
MF munter-style friction.
```

## Direction of tie

While staying on body part

```
->CR cranial (toward head), 
->CD caudal (toward feet),
->L left (of rigger)
->R right (of rigger)
->MD medial (towards the center)
->LT lateral (towards the outside)
```

Moving to body part
```
->FA to forearm
```

## Angle

Typically the angle of the rope leaving the previous tie or preparing for next.  Typically equivalenent to direction of tie

```
@12 (->CR) toward head
@6 (->CD) toward feet
@3 (->R) to the right
@9 (->L) to the left
``` 

