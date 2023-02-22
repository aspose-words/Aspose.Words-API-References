---
title: FileFormatUtil.LoadFormatToSaveFormat
second_title: Aspose.Words för .NET API Referens
description: FileFormatUtil metod. Konverterar enLoadFormat värde till aSaveFormat värde om möjligt.
type: docs
weight: 70
url: /sv/net/aspose.words/fileformatutil/loadformattosaveformat/
---
## FileFormatUtil.LoadFormatToSaveFormat method

Konverterar en[`LoadFormat`](../../loadformat/) värde till a[`SaveFormat`](../../saveformat/) värde om möjligt.

```csharp
public static SaveFormat LoadFormatToSaveFormat(LoadFormat loadFormat)
```

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentException | Kastar när det inte går att konvertera. |

### Exempel

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
* enum [LoadFormat](../../loadformat/)
* class [FileFormatUtil](../)
* namnutrymme [Aspose.Words](../../fileformatutil/)
* hopsättning [Aspose.Words](../../../)


