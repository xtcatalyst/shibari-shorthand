# Shibari Shorthand Notation v0.7

## Core Syntax
```

Rope            := RopeId ["." Length [UnitCode]]
Action          := Operation | Travel | Manipulation | Note | TensionNote

Operation       := Target ":" TechniqueList [Wraps] [ExitAngle] [TensionNote]
TechniqueList   := Technique { "|" Technique }
Technique       := (FrictionCode | TieCode) [ "." SurfaceCode | "." SideCode ] [Note]

Target          := PartCode [ "." SurfaceCode ] [ "." SideCode ]
Wraps           := "x" NUMBER [WrapDirCode]
ExitAngle       := "@" ClockAngle
TensionNote     := "t:" TensionLevel

Travel          := "->" ( Target | SurfaceCode  | Operation ) [Note]
Manipulation    := "+" Target "/" Target

Note            := "(" NoteBody ")"
NoteBody        := FreeText | NoteItem { "|" NoteItem }
NoteItem        := "nerve" | "pulse" | ("avoid:" Label) | ("pos:" Label)
```

## PartCode
`WR wrist | EL elbow | FA forearm UA upper arm | SH shoulder` 
`CHU upper chest | CHL lower chest | UB Under Bust| BU upper back | BL Lower Back | WA waist | HP hip`
`AN ankle | CF calf | KN knee | TH thigh | GR Groin`

## FrictionCode

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


