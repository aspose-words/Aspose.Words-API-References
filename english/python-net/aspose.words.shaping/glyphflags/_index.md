---
title: GlyphFlags enumeration
linktitle: GlyphFlags enumeration
articleTitle: GlyphFlags enumeration
second_title: Aspose.Words for Python
description: "aspose.words.shaping.GlyphFlags enumeration. Glyph flags."
type: docs
weight: 60
url: /python-net/aspose.words.shaping/glyphflags/
---

## GlyphFlags enumeration

Glyph flags.


### Members

| Name | Description |
| --- | --- |
| UNSAFE_TO_BREAK | Indicates that if input text is broken at the beginning of the cluster this glyph is part of, then both sides need to be re-shaped, as the result might be different. |
| UNSAFE_TO_CONCAT | Indicates that if input text is changed on one side of the beginning of the cluster this glyph is part of, then the shaping results for the other side might change. |
| SAFE_TO_INSERT_TATWEEL | In scripts that use elongation (Arabic, Mongolian, Syriac, etc.), this flag signifies that it is safe to insert a U+0640 TATWEEL character before this cluster for elongation. This flag does not determine the script-specific elongation places, but only when it is safe to do the elongation without interrupting text shaping. |

### See Also

* module [aspose.words.shaping](../)

