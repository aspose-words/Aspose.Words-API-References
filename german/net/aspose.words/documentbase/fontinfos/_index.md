---
title: DocumentBase.FontInfos
linktitle: FontInfos
articleTitle: FontInfos
second_title: Aspose.Words für .NET
description: Greifen Sie mit der FontInfos-Funktion von DocumentBase auf detaillierte Schrifteigenschaften zu und verbessern Sie mühelos das Design und die Lesbarkeit Ihres Dokuments.
type: docs
weight: 30
url: /de/net/aspose.words/documentbase/fontinfos/
---
## DocumentBase.FontInfos property

Bietet Zugriff auf die Eigenschaften der in diesem Dokument verwendeten Schriftarten.

```csharp
public FontInfoCollection FontInfos { get; }
```

## Bemerkungen

Diese Sammlung von Schriftartdefinitionen wird unverändert aus dem Dokument geladen. Schriftartdefinitionen können in einigen Dokumenten optional, fehlend oder unvollständig sein.

Verlassen Sie sich nicht auf diese Sammlung, um festzustellen, ob im Dokument eine bestimmte Schriftart verwendet wird. Sie sollten diese Sammlung nur verwenden, um Informationen zu Schriftarten zu erhalten, die möglicherweise im Dokument verwendet werden.

## Beispiele

Zeigt, wie ein Dokument mit eingebetteten TrueType-Schriftarten gespeichert wird.

```csharp
Document doc = new Document(MyDir + "Document.docx");

FontInfoCollection fontInfos = doc.FontInfos;
fontInfos.EmbedTrueTypeFonts = embedAllFonts;
fontInfos.EmbedSystemFonts = embedAllFonts;
fontInfos.SaveSubsetFonts = embedAllFonts;

doc.Save(ArtifactsDir + "Font.FontInfoCollection.docx");
```

Zeigt, wie Sie die Details der in einem Dokument vorhandenen Schriftarten ausdrucken.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Alle verwendeten und nicht verwendeten Schriftarten im Dokument drucken.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

### Siehe auch

* class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* class [DocumentBase](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
