---
title: ImportFormatOptions.IgnoreTextBoxes
second_title: Aspose.Words für .NET-API-Referenz
description: ImportFormatOptions eigendom. Ruft einen booleschen Wert ab oder legt diesen fest der angibt dass die Quellformatierung des Inhalts von Textfeldern ignoriert wird wennKeepSourceFormatting Modus wird verwendet. Der Standardwert istWAHR .
type: docs
weight: 50
url: /de/net/aspose.words/importformatoptions/ignoretextboxes/
---
## ImportFormatOptions.IgnoreTextBoxes property

Ruft einen booleschen Wert ab oder legt diesen fest, der angibt, dass die Quellformatierung des Inhalts von Textfeldern ignoriert wird wennKeepSourceFormatting Modus wird verwendet. Der Standardwert ist`WAHR` .

```csharp
public bool IgnoreTextBoxes { get; set; }
```

### Beispiele

Zeigt, wie Sie die Formatierung von Textfeldern beim Anhängen eines Dokuments verwalten.

```csharp
// Ein Dokument erstellen, in das Knoten aus einem anderen Dokument eingefügt werden.
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

builder.Writeln("Hello world!");

// Erstelle ein weiteres Dokument mit einem Textfeld, das wir in das erste Dokument importieren.
Document srcDoc = new Document();
builder = new DocumentBuilder(srcDoc);

Shape textBox = builder.InsertShape(ShapeType.TextBox, 300, 100);
builder.MoveTo(textBox.FirstParagraph);
builder.ParagraphFormat.Style.Font.Name = "Courier New";
builder.ParagraphFormat.Style.Font.Size = 24;
builder.Write("Textbox contents");

// Setzen Sie ein Flag, um anzugeben, ob die Textfeldformatierung gelöscht oder beibehalten werden soll
// beim Importieren in andere Dokumente.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreTextBoxes = ignoreTextBoxes;

// Importiere das Textfeld aus dem Quelldokument in das Zieldokument,
// und überprüfen Sie dann, ob wir den Stil des Textinhalts beibehalten haben.
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

### Siehe auch

* class [ImportFormatOptions](../)
* namensraum [Aspose.Words](../../importformatoptions/)
* Montage [Aspose.Words](../../../)


