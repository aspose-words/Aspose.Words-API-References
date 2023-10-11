---
title: ImportFormatOptions.IgnoreTextBoxes
second_title: Aspose.Words for .NET API Referansı
description: ImportFormatOptions mülk. Metin kutusu içeriğinin kaynak biçimlendirmesinin göz ardı edildiğini belirten bir boole değeri alır veya ayarlar ifKeepSourceFormatting modu kullanılır. Varsayılan değerdoğru .
type: docs
weight: 50
url: /tr/net/aspose.words/importformatoptions/ignoretextboxes/
---
## ImportFormatOptions.IgnoreTextBoxes property

Metin kutusu içeriğinin kaynak biçimlendirmesinin göz ardı edildiğini belirten bir boole değeri alır veya ayarlar ifKeepSourceFormatting modu kullanılır. Varsayılan değer:`doğru` .

```csharp
public bool IgnoreTextBoxes { get; set; }
```

### Örnekler

Belge eklerken metin kutusu formatının nasıl yönetileceğini gösterir.

```csharp
// Başka bir belgenin düğümlerinin ekleneceği bir belge oluşturun.
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

builder.Writeln("Hello world!");

// İlk belgeye aktaracağımız metin kutusuyla başka bir belge oluşturun.
Document srcDoc = new Document();
builder = new DocumentBuilder(srcDoc);

Shape textBox = builder.InsertShape(ShapeType.TextBox, 300, 100);
builder.MoveTo(textBox.FirstParagraph);
builder.ParagraphFormat.Style.Font.Name = "Courier New";
builder.ParagraphFormat.Style.Font.Size = 24;
builder.Write("Textbox contents");

// Metin kutusu formatının silineceğini veya korunacağını belirtmek için bir bayrak ayarlayın
// bunları diğer belgelere aktarırken.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreTextBoxes = ignoreTextBoxes;

// Metin kutusunu kaynak belgeden hedef belgeye aktarın,
// ve ardından metin içeriğinin stilini koruyup korumadığımızı doğrulayın.
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

### Ayrıca bakınız

* class [ImportFormatOptions](../)
* ad alanı [Aspose.Words](../../importformatoptions/)
* toplantı [Aspose.Words](../../../)


