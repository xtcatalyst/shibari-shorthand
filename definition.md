# Shibari Notation v0.5

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
`WR wrist | EL elbow | FA forearm UA upper arm | SH shoulder` 
`CHU upper chest | CHL lower chest | UB Under Bust| BU upper back | BL Lower Back | WA waist | HP hip`
`AN ankle | CF calf | KN knee | TH thigh | GR Groin`

## Cinch or Friction

`CP cinch pass | HH half-hitch | XF x-friction | SQ square knot | RF reverse friction |  MH munter hitch | MHR reverse munter hitch | CH cow hitch | LF l-friction | 360L 360 loop | LO lock off | OL open loop | UK ukki knot | TD tear drop`

## TieCode 

`SC single column | DC double column | RB rope band | HL half-lashing | HC hojo cuff | LH lark’s head as anchor `

## UnitCode

`ft | m | cm`

## FlagCode 

`!nerve | !pulse `

## SurfaceCode

`L left | R right | CR cranial | CD caudal | MD medial | LT lateral | V ventral | D dorsal`

## SideCode (Bottom/Model)

`L left | R right | B both (symmetric intent)`


