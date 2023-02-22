---
title: FieldRD.FileName
second_title: Aspose.Words for .NET API Referansı
description: FieldRD mülk. İçindekiler otoriteler tablosu veya dizin oluşturulurken dahil edilecek dosyanın adını alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldrd/filename/
---
## FieldRD.FileName property

İçindekiler, otoriteler tablosu veya dizin oluşturulurken dahil edilecek dosyanın adını alır veya ayarlar.

```csharp
public string FileName { get; set; }
```

### Örnekler

Diğer belgelerdeki başlıklardan içindekiler tablosu girdileri oluşturmak için RD alanını kullanmayı gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İçindekiler tablosu eklemek için bir belge oluşturucu kullanın,
// ve ardından sonraki sayfadaki içindekiler tablosu için bir giriş ekleyin.
builder.InsertField(FieldType.FieldTOC, true);
builder.InsertBreak(BreakType.PageBreak);
builder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
builder.Writeln("TOC entry from within this document");

// DosyaAdı özelliğinde başka bir yerel dosya sistemi belgesine başvuran bir RD alanı ekleyin.
// TOC artık referans verilen belgedeki tüm başlıkları kendi tablosu için girdi olarak kabul edecektir.
FieldRD field = (FieldRD)builder.InsertField(FieldType.FieldRefDoc, true);
field.FileName = "ReferencedDocument.docx";
field.IsPathRelative = true;

Assert.AreEqual(" RD  ReferencedDocument.docx \\f", field.GetFieldCode());

 // RD alanının referans aldığı belgeyi oluşturun ve bir başlık ekleyin.
// Bu başlık, ilk belgemizde TOC alanında bir giriş olarak görünecektir.
Document referencedDoc = new Document();
DocumentBuilder refDocBuilder = new DocumentBuilder(referencedDoc);
refDocBuilder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
refDocBuilder.Writeln("TOC entry from referenced document");
referencedDoc.Save(ArtifactsDir + "ReferencedDocument.docx");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.RD.docx");
```

### Ayrıca bakınız

* class [FieldRD](../)
* ad alanı [Aspose.Words.Fields](../../fieldrd/)
* toplantı [Aspose.Words](../../../)


