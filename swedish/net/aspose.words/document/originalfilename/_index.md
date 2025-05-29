---
title: Document.OriginalFileName
linktitle: OriginalFileName
articleTitle: OriginalFileName
second_title: Aspose.Words för .NET
description: Hämta det ursprungliga filnamnet på ditt dokument enkelt med egenskapen Dokumentets ursprungliga filnamn. Förbättra ditt arbetsflöde och din organisation idag!
type: docs
weight: 300
url: /sv/net/aspose.words/document/originalfilename/
---
## Document.OriginalFileName property

Hämtar dokumentets ursprungliga filnamn.

```csharp
public string OriginalFileName { get; }
```

## Anmärkningar

Returer`null` om dokumentet laddades från en ström eller skapades tomt.

## Exempel

Visar hur man hämtar information om ett dokuments inläsningsoperation.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(MyDir + "Document.docx", doc.OriginalFileName);
Assert.AreEqual(LoadFormat.Docx, doc.OriginalLoadFormat);
```

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

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
