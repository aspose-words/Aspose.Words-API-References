---
title: EmbeddedFontStyle Enum
linktitle: EmbeddedFontStyle
articleTitle: EmbeddedFontStyle
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words EmbeddedFontStyle-Aufzählung, um eingebettete Schriftstile in FontInfo-Objekten einfach zu verwalten und so Ihre Dokumentformatierungsfunktionen zu verbessern.
type: docs
weight: 3270
url: /de/net/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enumeration

Gibt den Stil einer eingebetteten Schriftart in einem[`FontInfo`](../fontinfo/) Objekt.

```csharp
[Flags]
public enum EmbeddedFontStyle
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Regular | `0` | Gibt die eingebettete Schriftart „Regular“ an. |
| Bold | `1` | Gibt die eingebettete Schriftart „Fett“ an. |
| Italic | `2` | Gibt die eingebettete Kursivschrift an. |
| BoldItalic | `3` | Gibt die eingebettete Schriftart Fett-Kursiv an. |

## Beispiele

Zeigt, wie eine eingebettete Schriftart aus einem Dokument extrahiert und im lokalen Dateisystem gespeichert wird.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Eingebettete Schriftformate können in anderen Formaten wie .doc unterschiedlich sein.
// Wir müssen das richtige Format kennen, bevor wir die Schriftart extrahieren können.
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// Außerdem können wir eingebettetes OpenType-Format, das aus .doc-Dokumenten stammt, in OpenType konvertieren.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### Siehe auch

* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)
