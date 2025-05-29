---
title: ImportFormatOptions.IgnoreTextBoxes
linktitle: IgnoreTextBoxes
articleTitle: IgnoreTextBoxes
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die ImportFormatOptions-Eigenschaft „IgnoreTextBoxes“ Ihre Dokumentformatierung durch die Steuerung des Textfeldinhalts verbessert. Optimieren Sie noch heute ganz einfach!
type: docs
weight: 50
url: /de/net/aspose.words/importformatoptions/ignoretextboxes/
---
## ImportFormatOptions.IgnoreTextBoxes property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, dass die Quellformatierung des Inhalts von Textfeldern ignoriert wird , wennKeepSourceFormatting Modus wird verwendet. Der Standardwert ist`WAHR` .

```csharp
public bool IgnoreTextBoxes { get; set; }
```

## Beispiele

Zeigt, wie die Textfeldformatierung beim Anhängen eines Dokuments verwaltet wird.

```csharp
// Erstellen Sie ein Dokument, in das Knoten aus einem anderen Dokument eingefügt werden.
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

builder.Writeln("Hello world!");

// Erstellen Sie ein weiteres Dokument mit einem Textfeld, das wir in das erste Dokument importieren.
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
// und überprüfen Sie dann, ob wir die Formatierung des Textinhalts beibehalten haben.
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
