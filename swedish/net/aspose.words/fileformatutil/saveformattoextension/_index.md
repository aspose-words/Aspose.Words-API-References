---
title: FileFormatUtil.SaveFormatToExtension
linktitle: SaveFormatToExtension
articleTitle: SaveFormatToExtension
second_title: Aspose.Words för .NET
description: Konvertera enkelt värden från sparade format till filändelser med FileFormatUtils SaveFormatToExtension-metod. Få exakta filändelser med gemener enkelt!
type: docs
weight: 80
url: /sv/net/aspose.words/fileformatutil/saveformattoextension/
---
## FileFormatUtil.SaveFormatToExtension method

Konverterar ett uppräknat värde i sparformat till en filändelse. Den returnerade filändelsen är en liten sträng med en inledande punkt.

```csharp
public static string SaveFormatToExtension(SaveFormat saveFormat)
```

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentException | Kastar när det inte går att konvertera. |

## Anmärkningar

DeWordML värdet konverteras till ".wml".

DeFlatOpc värdet konverteras till ".fopc".

## Exempel

Visar hur man använder FileFormatUtil-metoderna för att identifiera ett dokuments format.

```csharp
// Ladda ett dokument från en fil som saknar filändelse och identifiera sedan dess filformat.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Nedan följer två metoder för att konvertera ett LoadFormat till motsvarande SaveFormat.
    // 1 - Hämta filändelsen för LoadFormat och hämta sedan motsvarande SaveFormat från den strängen:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Konvertera LoadFormat direkt till dess SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Ladda ett dokument från strömmen och spara det sedan till den automatiskt upptäckta filändelsen.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Se även

* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
