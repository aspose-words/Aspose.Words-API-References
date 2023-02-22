---
title: DocumentBase.FontInfos
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBase eigendom. Bietet Zugriff auf Eigenschaften von Schriftarten die in diesem Dokument verwendet werden.
type: docs
weight: 30
url: /de/net/aspose.words/documentbase/fontinfos/
---
## DocumentBase.FontInfos property

Bietet Zugriff auf Eigenschaften von Schriftarten, die in diesem Dokument verwendet werden.

```csharp
public FontInfoCollection FontInfos { get; }
```

### Bemerkungen

Diese Sammlung von Schriftdefinitionen wird unverändert aus dem Dokument geladen. Schriftartdefinitionen können in einigen Dokumenten optional, fehlend oder unvollständig sein.

Verlassen Sie sich nicht auf diese Sammlung, um festzustellen, ob eine bestimmte Schriftart im Dokument verwendet wird. Sie sollten diese Sammlung nur verwenden, um Informationen über Schriftarten zu erhalten, die möglicherweise in dem Dokument verwendet werden.

### Beispiele

Zeigt, wie die Details zu den in einem Dokument vorhandenen Schriftarten gedruckt werden.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Drucken Sie alle verwendeten und nicht verwendeten Schriftarten im Dokument.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

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

* class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* class [DocumentBase](../)
* namensraum [Aspose.Words](../../documentbase/)
* Montage [Aspose.Words](../../../)


