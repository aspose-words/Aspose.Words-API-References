---
title: ImportFormatOptions.IgnoreTextBoxes
linktitle: IgnoreTextBoxes
articleTitle: IgnoreTextBoxes
second_title: .NET için Aspose.Words
description: ImportFormatOptions IgnoreTextBoxes özelliğinin metin kutusu içeriğini kontrol ederek belge biçimlendirmenizi nasıl geliştirdiğini keşfedin. Bugün kolayca optimize edin!
type: docs
weight: 50
url: /tr/net/aspose.words/importformatoptions/ignoretextboxes/
---
## ImportFormatOptions.IgnoreTextBoxes property

Metin kutusu içeriğinin kaynak biçimlendirmesinin yoksayıldığını belirten bir Boole değeri alır veya ayarlar eğerKeepSourceFormatting mod kullanılır. Varsayılan değer`doğru` .

```csharp
public bool IgnoreTextBoxes { get; set; }
```

## Örnekler

Bir belgeye ekleme yaparken metin kutusu biçimlendirmesinin nasıl yönetileceğini gösterir.

```csharp
// Başka bir belgeden düğümlerin ekleneceği bir belge oluşturun.
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

builder.Writeln("Hello world!");

// İlk belgeye aktaracağımız metin kutusu içeren başka bir belge oluşturalım.
Document srcDoc = new Document();
builder = new DocumentBuilder(srcDoc);

Shape textBox = builder.InsertShape(ShapeType.TextBox, 300, 100);
builder.MoveTo(textBox.FirstParagraph);
builder.ParagraphFormat.Style.Font.Name = "Courier New";
builder.ParagraphFormat.Style.Font.Size = 24;
builder.Write("Textbox contents");

// Metin kutusu biçimlendirmesini temizlemek mi yoksa korumak mı istediğinizi belirtmek için bir bayrak ayarlayın
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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
