# Syntax Definition

Pattern     := { Step }
Step        := Number ":" [Rope] Action { ";" Action }
Rope        := Letter ["." Length] // needed only for the first use of the rope
Action      := Bind | Travel | Note
Bind        := BodyPart ":" TT [Wraps] [WrapDir] [CinchOrFriction] [Angle] [Tension]
Travel      := -> Dest
Dest        := BodyPart [ "." Surface ]
Note        := "t:" Tension | "!nerve" | "!pulse" | "↔ mirror" | "[ ... ]" | "( ... ) xN"

BodyPart    := [code](#Body_Parts) [ "." Side [ "." Surface ] ]
Side        := "L" | "R" | "B"      // both = symmetrical intent
Surface     := "V" | "D"

TT          := "SC" | "DC" | "RB" | "HL" | "AL" | "CP"
Wraps       := "x" Number           // e.g., x2
WrapDir     := "cw" | "ccw"
CinchOrFriction := "CP" | "HH" | "XF" | "LK" | "SQ" | "MTR"
Angle       := "@" Clock
Clock       := "12"|"1"|"1:30"|...|"11:30"|"6"
Tension     := "soft"|"firm"|"tight"
Number      := integer
Manipulation := 

## Body Parts


