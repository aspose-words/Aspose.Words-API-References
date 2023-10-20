---
title: FileFormatUtil.SaveFormatToExtension
linktitle: SaveFormatToExtension
articleTitle: SaveFormatToExtension
second_title: Aspose.Words för .NET
description: FileFormatUtil SaveFormatToExtension metod. Konverterar ett sparat format uppräknat värde till ett filtillägg. Det returnerade tillägget är en sträng med små bokstäver med en inledande punkt i C#.
type: docs
weight: 80
url: /sv/net/aspose.words/fileformatutil/saveformattoextension/
---
## FileFormatUtil.SaveFormatToExtension method

Konverterar ett sparat format uppräknat värde till ett filtillägg. Det returnerade tillägget är en sträng med små bokstäver med en inledande punkt.

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

Visar hur du använder FileFormatUtil-metoderna för att upptäcka formatet på ett dokument.

```csharp
// Ladda ett dokument från en fil som saknar filtillägg, och identifiera sedan dess filformat.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Nedan finns två metoder för att konvertera ett LoadFormat till dess motsvarande SaveFormat.
    // 1 - Hämta filtilläggssträngen för LoadFormat och hämta sedan motsvarande SaveFormat från den strängen:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Konvertera LoadFormat direkt till dess SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Ladda ett dokument från strömmen och spara det sedan i det automatiskt upptäckta filtillägget.
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
