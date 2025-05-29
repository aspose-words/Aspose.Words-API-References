---
title: FontInfo.GetEmbeddedFontAsOpenType
linktitle: GetEmbeddedFontAsOpenType
articleTitle: GetEmbeddedFontAsOpenType
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die FontInfo-Methode GetEmbeddedFontAsOpenType eingebettete Schriftarten im OpenType-Format abruft und so Ihre Designflexibilität und -qualität verbessert.
type: docs
weight: 100
url: /de/net/aspose.words.fonts/fontinfo/getembeddedfontasopentype/
---
## FontInfo.GetEmbeddedFontAsOpenType method

Ruft eine eingebettete Schriftdatei im OpenType-Format ab. Schriftarten im Embedded OpenType-Format werden in OpenType konvertiert.

```csharp
public byte[] GetEmbeddedFontAsOpenType(EmbeddedFontStyle style)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
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

* enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* class [FontInfo](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
