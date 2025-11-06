---
title: GlyphFlags Enum
linktitle: GlyphFlags
articleTitle: GlyphFlags
second_title: Aspose.Words for .NET
description: Use GlyphFlags enum to control how individual glyphs are rendered and displayed during text shaping.
type: docs
weight: 6940
url: /net/aspose.words.shaping/glyphflags/
---
## GlyphFlags enumeration

Glyph flags.

```csharp
[Flags]
public enum GlyphFlags : byte
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| UnsafeToBreak | `1` | Indicates that if input text is broken at the beginning of the cluster this glyph is part of, then both sides need to be re-shaped, as the result might be different. |
| UnsafeToConcat | `2` | Indicates that if input text is changed on one side of the beginning of the cluster this glyph is part of, then the shaping results for the other side might change. |
| SafeToInsertTatweel | `4` | In scripts that use elongation (Arabic, Mongolian, Syriac, etc.), this flag signifies that it is safe to insert a U+0640 TATWEEL character before this cluster for elongation. This flag does not determine the script-specific elongation places, but only when it is safe to do the elongation without interrupting text shaping. |

### See Also

* namespace [Aspose.Words.Shaping](../../aspose.words.shaping/)
* assembly [Aspose.Words](../../)
