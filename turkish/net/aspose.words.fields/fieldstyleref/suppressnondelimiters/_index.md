---
title: FieldStyleRef.SuppressNonDelimiters
linktitle: SuppressNonDelimiters
articleTitle: SuppressNonDelimiters
second_title: Aspose.Words for .NET
description: FieldStyleRef SuppressNonDelimiters mülk. Sınırlayıcı olmayan karakterlerin gizlenip gizlenmeyeceğini alır veya ayarlar C#'da.
type: docs
weight: 80
url: /tr/net/aspose.words.fields/fieldstyleref/suppressnondelimiters/
---
## FieldStyleRef.SuppressNonDelimiters property

Sınırlayıcı olmayan karakterlerin gizlenip gizlenmeyeceğini alır veya ayarlar.

```csharp
public bool SuppressNonDelimiters { get; set; }
```

## Örnekler

STYLEREF alanlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Microsoft Word liste şablonunu kullanarak bir liste oluşturun.
Aspose.Words.Lists.List list = doc.Lists.Add(Aspose.Words.Lists.ListTemplate.NumberDefault);

// Oluşturulan bu listede "1.a )" görüntülenecektir.
 // Parantezden önceki boşluk, sınırlayıcı olmayan bir karakterdir ve bunu bastırabiliriz.
list.ListLevels[0].NumberFormat = "\x0000.";
list.ListLevels[1].NumberFormat = "\x0001 )";

// Metin ekleyin ve STYLEREF alanlarının referans alacağı paragraf stillerini uygulayın.
builder.ListFormat.List = list;
builder.ListFormat.ListIndent();
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 1");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln("Item 2");
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 3");
builder.ListFormat.RemoveNumbers();
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Başlığa bir STYLEREF alanı yerleştirin ve belgedeki ilk "Paragraf Listele" stilindeki metni görüntüleyin.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
FieldStyleRef field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";

// Altbilgiye bir STYLEREF alanı yerleştirin ve son metni görüntülemesini sağlayın.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";
field.SearchFromBottom = true;

builder.MoveToDocumentEnd();

// Listelerin liste numaralarına referans vermek için STYLEREF alanlarını da kullanabiliriz.
builder.Write("\nParagraph number: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumber = true;

builder.Write("\nParagraph number, relative context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInRelativeContext = true;

builder.Write("\nParagraph number, full context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;

builder.Write("\nParagraph number, full context, non-delimiter chars suppressed: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;
field.SuppressNonDelimiters = true;

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.STYLEREF.docx");
```

### Ayrıca bakınız

* class [FieldStyleRef](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
