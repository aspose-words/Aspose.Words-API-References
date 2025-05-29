---
title: FontInfo.GetEmbeddedFont
linktitle: GetEmbeddedFont
articleTitle: GetEmbeddedFont
second_title: Aspose.Words für .NET
description: Entdecken Sie die FontInfo GetEmbeddedFont-Methode zum einfachen Abrufen bestimmter eingebetteter Schriftdateien und verbessern Sie Ihre Designprojekte mit nahtloser Typografie.
type: docs
weight: 90
url: /de/net/aspose.words.fonts/fontinfo/getembeddedfont/
---
## FontInfo.GetEmbeddedFont method

Ruft eine bestimmte eingebettete Schriftartdatei ab.

```csharp
public byte[] GetEmbeddedFont(EmbeddedFontFormat format, EmbeddedFontStyle style)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| format | EmbeddedFontFormat | Gibt das abzurufende Schriftformat an. |
| style | EmbeddedFontStyle | Gibt den abzurufenden Schriftstil an. |

### Rückgabewert

Rückgaben`null` wenn die angegebene Schriftart nicht eingebettet ist.

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

* enum [EmbeddedFontFormat](../../embeddedfontformat/)
* enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* class [FontInfo](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
