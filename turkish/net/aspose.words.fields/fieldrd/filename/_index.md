---
title: FieldRD.FileName
second_title: Aspose.Words for .NET API Referansı
description: FieldRD mülk. İçindekiler tablosu yetki tablosu veya dizin oluşturulurken eklenecek dosyanın adını alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldrd/filename/
---
## FieldRD.FileName property

İçindekiler tablosu, yetki tablosu veya dizin oluşturulurken eklenecek dosyanın adını alır veya ayarlar.

```csharp
public string FileName { get; set; }
```

### Örnekler

Diğer belgelerdeki başlıklardan bir içindekiler tablosu girişleri oluşturmak için RD alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İçindekiler tablosu eklemek için bir belge oluşturucu kullanın,
// ve ardından sonraki sayfadaki içindekiler tablosu için bir giriş ekleyin.
builder.InsertField(FieldType.FieldTOC, true);
builder.InsertBreak(BreakType.PageBreak);
builder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
builder.Writeln("TOC entry from within this document");

// FileName özelliğinde başka bir yerel dosya sistemi belgesine başvuran bir RD alanı ekleyin.
// TOC artık başvurulan belgedeki tüm başlıkları kendi tablosuna giriş olarak kabul edecektir.
FieldRD field = (FieldRD)builder.InsertField(FieldType.FieldRefDoc, true);
field.FileName = ArtifactsDir + "ReferencedDocument.docx";

Assert.AreEqual($" RD  {ArtifactsDir.Replace(@"\",@"\\")}ReferencedDocument.docx", field.GetFieldCode());

 // RD alanının referans aldığı belgeyi oluşturun ve bir başlık ekleyin.
// Bu başlık ilk belgemizdeki TOC alanında bir giriş olarak görünecektir.
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


