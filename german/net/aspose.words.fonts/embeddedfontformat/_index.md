---
title: EmbeddedFontFormat Enum
linktitle: EmbeddedFontFormat
articleTitle: EmbeddedFontFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.EmbeddedFontFormat, die die Formate eingebetteter Schriftarten im FontInfo-Objekt für eine verbesserte Dokumentgestaltung definiert.
type: docs
weight: 3260
url: /de/net/aspose.words.fonts/embeddedfontformat/
---
## EmbeddedFontFormat enumeration

Gibt das Format einer bestimmten eingebetteten Schriftart an[`FontInfo`](../fontinfo/) Objekt.

Beim Speichern eines Dokuments in einer Datei werden nur eingebettete Schriftarten des entsprechenden Formats mitgeschrieben.

```csharp
public enum EmbeddedFontFormat
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| EmbeddedOpenType | `0` | Gibt das Embedded OpenType (EOT)-Dateiformat an. |
| OpenType | `1` | Gibt die Schriftart an, die als einfache Kopie einer OpenType-Schriftartdatei (TrueType) eingebettet ist. |

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
