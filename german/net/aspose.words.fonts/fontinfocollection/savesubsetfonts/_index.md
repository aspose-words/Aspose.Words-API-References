---
title: FontInfoCollection.SaveSubsetFonts
second_title: Aspose.Words für .NET-API-Referenz
description: FontInfoCollection eigendom. Gibt an ob eine Teilmenge der eingebetteten TrueTypeSchriftarten mit dem Dokument gespeichert werden soll oder nicht. Der Standardwert für diese Eigenschaft ist FALSCH.
type: docs
weight: 50
url: /de/net/aspose.words.fonts/fontinfocollection/savesubsetfonts/
---
## FontInfoCollection.SaveSubsetFonts property

Gibt an, ob eine Teilmenge der eingebetteten TrueType-Schriftarten mit dem Dokument gespeichert werden soll oder nicht. Der Standardwert für diese Eigenschaft ist **FALSCH**.

Diese Option funktioniert nur, wenn[`EmbedTrueTypeFonts`](../embedtruetypefonts/) Eigenschaft eingestellt ist **Stimmt**.

```csharp
public bool SaveSubsetFonts { get; set; }
```

### Bemerkungen

Diese Option funktioniert nur für die Formate DOC, DOCX und RTF.

### Beispiele

Zeigt, wie ein Dokument mit eingebetteten TrueType-Schriftarten gespeichert wird.

```csharp
Document doc = new Document(MyDir + "Document.docx");

FontInfoCollection fontInfos = doc.FontInfos;
fontInfos.EmbedTrueTypeFonts = embedAllFonts;
fontInfos.EmbedSystemFonts = embedAllFonts;
fontInfos.SaveSubsetFonts = embedAllFonts;

doc.Save(ArtifactsDir + "Font.FontInfoCollection.docx");

if (embedAllFonts)
    Assert.That(25000, Is.LessThan(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
else
    Assert.That(15000, Is.AtLeast(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
```

### Siehe auch

* class [FontInfoCollection](../)
* namensraum [Aspose.Words.Fonts](../../fontinfocollection/)
* Montage [Aspose.Words](../../../)


