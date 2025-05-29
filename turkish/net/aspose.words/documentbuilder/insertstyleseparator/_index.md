---
title: DocumentBuilder.InsertStyleSeparator
linktitle: InsertStyleSeparator
articleTitle: InsertStyleSeparator
second_title: .NET için Aspose.Words
description: Belgelerinizi DocumentBuilder InsertStyleSeparator yöntemiyle geliştirin; gelişmiş biçimlendirme ve düzenleme için stil ayırıcıları zahmetsizce ekleyin.
type: docs
weight: 490
url: /tr/net/aspose.words/documentbuilder/insertstyleseparator/
---
## DocumentBuilder.InsertStyleSeparator method

Belgeye stil ayırıcı ekler.

```csharp
public void InsertStyleSeparator()
```

## Notlar

Bu yöntem, bir metin satırının iki farklı bölümüne farklı paragraf stilleri uygulanmasına olanak tanır.

## Örnekler

Stil ayırıcılarla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Her paragrafın yalnızca bir stili olabilir.
// InsertStyleSeparator metodu bu sınırlamayı aşmamızı sağlar.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Write("This text is in a Heading style. ");
builder.InsertStyleSeparator();

Style paraStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyParaStyle");
paraStyle.Font.Bold = false;
paraStyle.Font.Size = 8;
paraStyle.Font.Name = "Arial";

builder.ParagraphFormat.StyleName = paraStyle.Name;
builder.Write("This text is in a custom style. ");

// InsertStyleSeparator metodunu çağırmak başka bir paragraf oluşturur,
// öncekinden farklı bir stile sahip olabilir. Paragraflar arasında ara olmayacak.
// Çıktı belgesindeki metin iki stile sahip tek bir paragraf gibi görünecektir.
Assert.AreEqual(2, doc.FirstSection.Body.Paragraphs.Count);
Assert.AreEqual("Heading 1", doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.Style.Name);
Assert.AreEqual("MyParaStyle", doc.FirstSection.Body.Paragraphs[1].ParagraphFormat.Style.Name);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertStyleSeparator.docx");
```

### Ayrıca bakınız

* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
