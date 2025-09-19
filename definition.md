# Shibari Notation v0.4

## Core Syntax
```
Rope           := RopeId ["." Length [UnitCode]]
Action         := Bind | FrictionFix | Travel | Manipulation | Note | TensionNote
Bind           := Target ":" TieSpec [Wraps]  [ExitAngle] [TensionNote]

FrictionFix    := Target ":" FrictionCode [ExitAngle] [TensionNote]
TieSpec        := TieCode [ "." DirectionCode ]          
Target         := PartCode [ "." SideCode ] [ "." SurfaceCode ] 
Wraps          := "x" NUMBER
WrapDirCode    := "cw" | "ccw"
ExitAngle      := "@" ClockAngle              // attaches to the immediately preceding Bind/FrictionFix
TensionNote    := "t:" TensionLevel
Travel         := "->" ( Target | SurfaceCode )

Manipulation   := "+" Target "/" Target       // bring/hold two targets together

Note           := FlagCode | MirrorKeyword | BracketNote | TypedNote
BracketNote    := "[" FreeText "]"            // e.g., [sternal gap], [below shoulder blades]
TypedNote      := "(" NoteItem { "|" NoteItem } ")"
NoteItem       := "nerve" | "pulse" | ("avoid:" Label) | ("pos:" Label)
```

## PartCode

`WR wrist | AN ankle | FA forearm | UA upper arm | EL elbow | CHU upper chest | CHL lower chest | WA waist | HP hip | TH thigh | KN knee | CF calf | NK neck | RB ribcage |  SH shoulder | BU back up | BL back lower`

## Cinch or Friction

`CP cinch pass | HH half-hitch | XF X-friction | LHF lark’s head friction | SQ (square knot) | RF (reverse friction) |  MH munter hitch | MHR reverse munter hitch | CH Cow Hitch | LF L-Friction | 360L 360 Loop | LO lock off`

## TieCode 

`SC single column | DC double column | RB rope band | HL half-lashing | LHA anchor lark’s head), HC (Hojo cuff)`

## UnitCode

`ft | m | cm`

FlagCode 

`!nerve | !pulse | <> mirror`

SurfaceCode

`L left | R right | CR cranial | CD caudal | MD medial | LT lateral | V ventral | D dorsal`

SideCode (Bottom/Model)

`L left | R right | B both (symmetric intent)`


