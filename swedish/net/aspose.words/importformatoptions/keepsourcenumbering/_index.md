---
title: ImportFormatOptions.KeepSourceNumbering
linktitle: KeepSourceNumbering
articleTitle: KeepSourceNumbering
second_title: Aspose.Words för .NET
description: Styr dokumentnumrering med egenskapen ImportFormatOptions KeepSourceNumbering. Hantera enkelt kollisioner för sömlös import. Standardvärde: falskt.
type: docs
weight: 60
url: /sv/net/aspose.words/importformatoptions/keepsourcenumbering/
---
## ImportFormatOptions.KeepSourceNumbering property

Hämtar eller ställer in ett booleskt värde som anger hur numreringen ska importeras när den kolliderar i käll- och destinationsdokument. Standardvärdet är`falsk` .

```csharp
public bool KeepSourceNumbering { get; set; }
```

## Exempel

Visar hur man löser en konflikt vid import av dokument som har listor med samma listdefinitionsidentifierare.

```csharp
Document srcDoc = new Document(MyDir + "List with the same definition identifier - source.docx");
Document dstDoc = new Document(MyDir + "List with the same definition identifier - destination.docx");

// Sätt egenskapen "KeepSourceNumbering" till "true" för att använda ett annat listdefinitions-ID
// till identiska stilar som Aspose.Words importerar dem till destinationsdokument.
ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };

dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, importFormatOptions);
dstDoc.UpdateListLabels();
```

Visar hur man importerar ett dokument med numrerade listor.

```csharp
Document srcDoc = new Document(MyDir + "List source.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

Assert.AreEqual(4, dstDoc.Lists.Count);

ImportFormatOptions options = new ImportFormatOptions();

// Om det finns en konflikt mellan listformaten, använd källdokumentets listformat.
// Sätt egenskapen "KeepSourceNumbering" till "false" för att inte importera några listnummer till destinationsdokumentet.
// Sätt egenskapen "KeepSourceNumbering" till "true" importera alla kollisioner
// listformatnumrering med samma utseende som den hade i källdokumentet.
options.KeepSourceNumbering = isKeepSourceNumbering;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);
dstDoc.UpdateListLabels();

Assert.AreEqual(isKeepSourceNumbering ? 5 : 4, dstDoc.Lists.Count);
```

Visar hur man löser konflikter mellan listnumreringar i käll- och måldokument.

```csharp
// Öppna ett dokument med ett anpassat listnumreringsschema och klona det sedan.
// Eftersom båda har samma numreringsformat kommer formaten att krocka om vi importerar det ena dokumentet till det andra.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// När vi importerar dokumentets klon till originalet och sedan lägger till den,
// då kommer de två listorna med samma listformat att sammanfogas.
// Om vi ställer in flaggan "KeepSourceNumbering" till "false", så klonas listan från dokumentet
// som vi lägger till i originalet kommer att fortsätta numreringen av listan vi lägger till den i.
// Detta kommer effektivt att slå samman de två listorna till en.
// Om vi ställer in flaggan "KeepSourceNumbering" till "true", så klonas dokumentet
 // list behåller sin ursprungliga numrering, vilket gör att de två listorna visas som separata listor.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.KeepSourceNumbering = keepSourceNumbering;

NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepDifferentStyles, importFormatOptions);
foreach (Paragraph paragraph in srcDoc.FirstSection.Body.Paragraphs)
{
    Node importedNode = importer.ImportNode(paragraph, true);
    dstDoc.FirstSection.Body.AppendChild(importedNode);
}

dstDoc.UpdateListLabels();

if (keepSourceNumbering)
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
else
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "10. Item 1\r\n" +
        "11. Item 2 \r\n" +
        "12. Item 3\r\n" +
        "13. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
```

### Se även

* class [ImportFormatOptions](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
