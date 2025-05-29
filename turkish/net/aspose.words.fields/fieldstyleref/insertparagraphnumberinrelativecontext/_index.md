---
title: FieldStyleRef.InsertParagraphNumberInRelativeContext
linktitle: InsertParagraphNumberInRelativeContext
articleTitle: InsertParagraphNumberInRelativeContext
second_title: .NET için Aspose.Words
description: Belgelerinizdeki paragraf numaralandırmasını daha kolay yönetmek ve daha anlaşılır hale getirmek için FieldStyleRef InsertParagraphNumberInRelativeContext özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.fields/fieldstyleref/insertparagraphnumberinrelativecontext/
---
## FieldStyleRef.InsertParagraphNumberInRelativeContext property

Başvurulan paragrafın paragraf numarasının bağıl bağlamda eklenip eklenmeyeceğini alır veya ayarlar.

```csharp
public bool InsertParagraphNumberInRelativeContext { get; set; }
```

## Örnekler

STYLEREF alanlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Microsoft Word liste şablonunu kullanarak bir liste oluşturun.
Aspose.Words.Lists.List list = doc.Lists.Add(Aspose.Words.Lists.ListTemplate.NumberDefault);

// Oluşturulan bu listede "1.a )" gösterilecektir.
 // Parantezden önceki boşluk, sınırlayıcı olmayan bir karakterdir ve bunu bastırabiliriz.
list.ListLevels[0].NumberFormat = "\x0000.";
list.ListLevels[1].NumberFormat = "\x0001 )";

// STYLEREF alanlarının başvuracağı metni ekleyin ve paragraf stilleri uygulayın.
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

// Başlığa bir STYLEREF alanı yerleştirin ve belgedeki ilk "Liste Paragrafı" stilindeki metni görüntüleyin.
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
