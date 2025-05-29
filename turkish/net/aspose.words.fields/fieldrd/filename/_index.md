---
title: FieldRD.FileName
linktitle: FileName
articleTitle: FileName
second_title: .NET için Aspose.Words
description: FieldRD FileName özelliğinin, içindekiler tablonuzu ve dizinlerinizi oluşturmak için adları kolayca ayarlayarak dosya yönetimini nasıl basitleştirdiğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldrd/filename/
---
## FieldRD.FileName property

İçindekiler tablosu, yetki tablosu veya dizin oluştururken eklenecek dosyanın adını alır veya ayarlar.

```csharp
public string FileName { get; set; }
```

## Örnekler

Diğer belgelerdeki başlıklardan bir içerik tablosu girişi oluşturmak için RD alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İçindekiler tablosu eklemek için bir belge oluşturucu kullanın,
// ve ardından bir sonraki sayfadaki içerik tablosuna bir giriş ekleyin.
builder.InsertField(FieldType.FieldTOC, true);
builder.InsertBreak(BreakType.PageBreak);
builder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
builder.Writeln("TOC entry from within this document");

// FileName özelliğinde başka bir yerel dosya sistemi belgesine başvuran bir RD alanı ekleyin.
// İçindekiler tablosu artık başvurulan belgedeki tüm başlıkları tablosuna giriş olarak kabul edecektir.
FieldRD field = (FieldRD)builder.InsertField(FieldType.FieldRefDoc, true);
field.FileName = ArtifactsDir + "ReferencedDocument.docx";

Assert.AreEqual($" RD  {ArtifactsDir.Replace(@"\",@"\\")}ReferencedDocument.docx", field.GetFieldCode());

 // RD alanının başvurduğu belgeyi oluştur ve bir başlık ekle.
// Bu başlık ilk belgemizin İçindekiler alanında bir giriş olarak gösterilecektir.
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
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
