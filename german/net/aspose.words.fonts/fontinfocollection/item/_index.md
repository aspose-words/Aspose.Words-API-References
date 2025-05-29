---
title: FontInfoCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words für .NET
description: Entdecken Sie die FontInfoCollection-Elementeigenschaft, um Schriftarten einfach nach Namen abzurufen und Ihre Designprojekte mit Präzision und Stil zu verbessern.
type: docs
weight: 40
url: /de/net/aspose.words.fonts/fontinfocollection/item/
---
## FontInfoCollection indexer (1 of 2)

Ruft eine Schriftart mit dem angegebenen Namen ab.

```csharp
public FontInfo this[string name] { get; }
```

| Parameter | Beschreibung |
| --- | --- |
| name | Name der zu suchenden Schriftart ohne Berücksichtigung der Groß-/Kleinschreibung. |

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

* class [FontInfo](../../fontinfo/)
* class [FontInfoCollection](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)

---

## FontInfoCollection indexer (2 of 2)

Ruft eine Schriftart am angegebenen Index ab.

```csharp
public FontInfo this[int index] { get; }
```

| Parameter | Beschreibung |
| --- | --- |
| index | Nullbasierter Index der Schriftart. |

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

* class [FontInfo](../../fontinfo/)
* class [FontInfoCollection](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
