## Toll the Dead
```GN
!servalias toll embed
{{set("mod", max(charismaMod, wisdomMod, intelligenceMod))}}
{{set("y", 4 if level > 16 else 3 if level > 10 else 2 if level > 4 else 1)}}
{{set("z", vroll(str(y)+"d8"))}}
{{set("Z", vroll(str(y)+"d12"))}}
-title "<name> casts Toll the Dead!"
-desc "<name> points at one creature they can see within range (60ft), and the sound of a dolorous bell fills the air around it for a moment. The target must succeed on a DC{{mod+8+proficiencyBonus}} Wisdom saving throw or take {{y}}d8 necrotic damage. If the target is missing any of its hit points, it instead takes {{y}}d12 necrotic damage."
-f "Undamaged | {{z}} if they fail"
-f "Damaged | {{Z}} if they fail"
-color <color> -thumb <image>
```