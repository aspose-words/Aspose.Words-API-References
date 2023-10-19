---
title: DocumentBuilder.InsertStyleSeparator
linktitle: InsertStyleSeparator
articleTitle: InsertStyleSeparator
second_title: Aspose.Words for .NET
description: DocumentBuilder InsertStyleSeparator yöntem. Belgeye stil ayırıcıyı ekler C#'da.
type: docs
weight: 450
url: /tr/net/aspose.words/documentbuilder/insertstyleseparator/
---
## DocumentBuilder.InsertStyleSeparator method

Belgeye stil ayırıcıyı ekler.

```csharp
public void InsertStyleSeparator()
```

## Notlar

Bu yöntem, bir metin satırının iki farklı bölümüne farklı paragraf stillerinin uygulanmasına olanak tanır.

## Örnekler

Stil ayırıcılarla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Her paragrafın yalnızca bir stili olabilir.
// InsertStyleSeparator yöntemi bu sınırlamayı aşmamıza olanak tanır.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Write("This text is in a Heading style. ");
builder.InsertStyleSeparator();

Style paraStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyParaStyle");
paraStyle.Font.Bold = false;
paraStyle.Font.Size = 8;
paraStyle.Font.Name = "Arial";

builder.ParagraphFormat.StyleName = paraStyle.Name;
builder.Write("This text is in a custom style. ");

// InsertStyleSeparator yöntemini çağırmak başka bir paragraf oluşturur,
// öncekinden farklı bir stile sahip olabilir. Paragraflar arasında boşluk verilmeyecektir.
// Çıktı belgesindeki metin, iki stile sahip bir paragraf gibi görünecektir.
Assert.AreEqual(2, doc.FirstSection.Body.Paragraphs.Count);
Assert.AreEqual("Heading 1", doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.Style.Name);
Assert.AreEqual("MyParaStyle", doc.FirstSection.Body.Paragraphs[1].ParagraphFormat.Style.Name);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertStyleSeparator.docx");
```

### Ayrıca bakınız

* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
