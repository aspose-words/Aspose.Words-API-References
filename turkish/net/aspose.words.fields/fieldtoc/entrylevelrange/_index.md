---
title: FieldToc.EntryLevelRange
linktitle: EntryLevelRange
articleTitle: EntryLevelRange
second_title: .NET için Aspose.Words
description: Gelişmiş gezinme ve kullanıcı deneyimi için içerik seviyelerinizi kolayca özelleştirmek üzere FieldToc EntryLevelRange özelliğini keşfedin.
type: docs
weight: 60
url: /tr/net/aspose.words.fields/fieldtoc/entrylevelrange/
---
## FieldToc.EntryLevelRange property

İçindekiler tablosu girişlerinin dahil edilecek seviye aralığını alır veya ayarlar.

```csharp
public string EntryLevelRange { get; set; }
```

## Örnekler

İçindekiler alanının nasıl ekleneceğini ve hangi TC alanlarının giriş olarak sonuçlanacağının nasıl filtreleneceğini gösterir.

```csharp
public void FieldTocEntryIdentifier()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // İçindekiler tablosuna tüm TC alanlarını derleyecek bir İçindekiler alanı ekleyin.
    FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Alanı yalnızca "A" türündeki TC girişlerini ve 1 ile 3 arasındaki giriş düzeyini alacak şekilde yapılandırın.
    fieldToc.EntryIdentifier = "A";
    fieldToc.EntryLevelRange = "1-3";

    Assert.AreEqual(" TOC  \\f A \\l 1-3", fieldToc.GetFieldCode());

    // Bu iki giriş tabloda görünecektir.
    builder.InsertBreak(BreakType.PageBreak);
    InsertTocEntry(builder, "TC field 1", "A", "1");
    InsertTocEntry(builder, "TC field 2", "A", "2");

    Assert.AreEqual(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.Range.Fields[1].GetFieldCode());

    // Bu girdi "A"dan farklı bir türe sahip olduğundan tablodan çıkarılacak.
    InsertTocEntry(builder, "TC field 3", "B", "1");

    // Bu girdi, 1-3 aralığının dışında bir giriş seviyesine sahip olduğundan tablodan çıkarılacaktır.
    InsertTocEntry(builder, "TC field 4", "A", "5");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TC.docx");
}

/// <summary>
/// TC alanı eklemek için bir belge oluşturucu kullanın.
/// </summary>
public void InsertTocEntry(DocumentBuilder builder, string text, string typeIdentifier, string entryLevel)
{
    FieldTC fieldTc = (FieldTC)builder.InsertField(FieldType.FieldTOCEntry, true);
    fieldTc.OmitPageNumber = true;
    fieldTc.Text = text;
    fieldTc.TypeIdentifier = typeIdentifier;
    fieldTc.EntryLevel = entryLevel;
}
```

### Ayrıca bakınız

* class [FieldToc](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
