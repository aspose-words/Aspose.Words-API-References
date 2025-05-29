---
title: ImportFormatOptions.IgnoreTextBoxes
linktitle: IgnoreTextBoxes
articleTitle: IgnoreTextBoxes
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen ImportFormatOptions IgnoreTextBoxes förbättrar formateringen av ditt dokument genom att kontrollera textruteinnehållet. Optimera enkelt idag!
type: docs
weight: 50
url: /sv/net/aspose.words/importformatoptions/ignoretextboxes/
---
## ImportFormatOptions.IgnoreTextBoxes property

Hämtar eller ställer in ett booleskt värde som anger att källformateringen av textrutes innehåll ignoreras omKeepSourceFormatting läget används. Standardvärdet är`sann` .

```csharp
public bool IgnoreTextBoxes { get; set; }
```

## Exempel

Visar hur man hanterar formatering av textrutor när man lägger till ett dokument.

```csharp
// Skapa ett dokument som ska ha noder från ett annat dokument infogade i det.
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

builder.Writeln("Hello world!");

// Skapa ett annat dokument med en textruta, som vi importerar till det första dokumentet.
Document srcDoc = new Document();
builder = new DocumentBuilder(srcDoc);

Shape textBox = builder.InsertShape(ShapeType.TextBox, 300, 100);
builder.MoveTo(textBox.FirstParagraph);
builder.ParagraphFormat.Style.Font.Name = "Courier New";
builder.ParagraphFormat.Style.Font.Size = 24;
builder.Write("Textbox contents");

// Ange en flagga för att ange om textrutans formatering ska raderas eller bevaras
// när de importeras till andra dokument.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreTextBoxes = ignoreTextBoxes;

// Importera textrutan från källdokumentet till destinationsdokumentet,
// och sedan verifiera om vi har bevarat formateringen av dess textinnehåll.
NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);
Shape importedTextBox = (Shape)importer.ImportNode(textBox, true);
dstDoc.FirstSection.Body.Paragraphs[1].AppendChild(importedTextBox);

if (ignoreTextBoxes)
{
    Assert.AreEqual(12.0d, importedTextBox.FirstParagraph.Runs[0].Font.Size);
    Assert.AreEqual("Times New Roman", importedTextBox.FirstParagraph.Runs[0].Font.Name);
}
else
{
    Assert.AreEqual(24.0d, importedTextBox.FirstParagraph.Runs[0].Font.Size);
    Assert.AreEqual("Courier New", importedTextBox.FirstParagraph.Runs[0].Font.Name);
}

dstDoc.Save(ArtifactsDir + "DocumentBuilder.IgnoreTextBoxes.docx");
```

### Se även

* class [ImportFormatOptions](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
