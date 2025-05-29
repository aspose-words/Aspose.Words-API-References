---
title: FileFormatUtil.LoadFormatToExtension
linktitle: LoadFormatToExtension
articleTitle: LoadFormatToExtension
second_title: Aspose.Words för .NET
description: Omvandla enkelt värden från laddningsformat till filändelser med FileFormatUtils LoadFormatToExtension-metod. Få exakta filändelser med gemener enkelt!
type: docs
weight: 60
url: /sv/net/aspose.words/fileformatutil/loadformattoextension/
---
## FileFormatUtil.LoadFormatToExtension method

Konverterar ett uppräknat värde i laddningsformat till en filändelse. Den returnerade filändelsen är en liten sträng med en inledande punkt.

```csharp
public static string LoadFormatToExtension(LoadFormat loadFormat)
```

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentException | Kastar när det inte går att konvertera. |

## Anmärkningar

DeWordML värdet konverteras till ".wml".

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

* enum [LoadFormat](../../loadformat/)
* class [FileFormatUtil](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
