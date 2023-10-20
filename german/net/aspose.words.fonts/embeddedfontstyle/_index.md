---
title: EmbeddedFontStyle Enum
linktitle: EmbeddedFontStyle
articleTitle: EmbeddedFontStyle
second_title: Aspose.Words für .NET
description: Aspose.Words.Fonts.EmbeddedFontStyle opsomming. Gibt den Stil einer eingebetteten Schriftart in a anFontInfo Objekt in C#.
type: docs
weight: 2860
url: /de/net/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enumeration

Gibt den Stil einer eingebetteten Schriftart in a an[`FontInfo`](../fontinfo/) Objekt.

```csharp
[Flags]
public enum EmbeddedFontStyle
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Regular | `0` | Gibt die eingebettete reguläre Schriftart an. |
| Bold | `1` | Gibt die eingebettete Schriftart Bold an. |
| Italic | `2` | Gibt die eingebettete Kursivschrift an. |
| BoldItalic | `3` | Gibt die eingebettete Schriftart „Fett-Kursiv“ an. |

## Beispiele

Zeigt, wie man eine eingebettete Schriftart aus einem Dokument extrahiert und im lokalen Dateisystem speichert.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Eingebettete Schriftartformate können in anderen Formaten wie .doc unterschiedlich sein.
// Wir müssen das richtige Format kennen, bevor wir die Schriftart extrahieren können.
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// Außerdem können wir das eingebettete OpenType-Format, das aus .doc-Dokumenten stammt, in OpenType konvertieren.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### Siehe auch

* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)
