---
title: FieldRD.IsPathRelative
linktitle: IsPathRelative
articleTitle: IsPathRelative
second_title: .NET için Aspose.Words
description: Belge yollarını kolayca yönetmek için FieldRD'nin IsPathRelative özelliğini keşfedin. Gelişmiş verimlilik için esnek yol ayarlarıyla kodlamanızı basitleştirin!
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldrd/ispathrelative/
---
## FieldRD.IsPathRelative property

Yolun geçerli belgeye göreli olup olmadığını alır veya ayarlar.

```csharp
public bool IsPathRelative { get; set; }
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
