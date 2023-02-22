---
title: FieldToc.EntryLevelRange
second_title: Aspose.Words for .NET API Referansı
description: FieldToc mülk. Dahil edilecek içindekiler tablosu girişlerinin bir dizi düzeyini alır veya ayarlar.
type: docs
weight: 60
url: /tr/net/aspose.words.fields/fieldtoc/entrylevelrange/
---
## FieldToc.EntryLevelRange property

Dahil edilecek içindekiler tablosu girişlerinin bir dizi düzeyini alır veya ayarlar.

```csharp
public string EntryLevelRange { get; set; }
```

### Örnekler

İçindekiler alanının nasıl ekleneceğini ve hangi TC alanlarının giriş olarak sonuçlanacağını filtreler.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Tüm TC alanlarını bir içindekiler tablosunda derleyecek bir TOC alanı ekleyin.
    FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Alanı yalnızca "A" tipi TC girişlerini ve 1 ile 3 arasında bir giriş seviyesi alacak şekilde yapılandırın.
    fieldToc.EntryIdentifier = "A";
    fieldToc.EntryLevelRange = "1-3";

    Assert.AreEqual(" TOC  \\f A \\l 1-3", fieldToc.GetFieldCode());

    // Bu iki giriş tabloda görünecektir.
    builder.InsertBreak(BreakType.PageBreak);
    InsertTocEntry(builder, "TC field 1", "A", "1");
    InsertTocEntry(builder, "TC field 2", "A", "2");

    Assert.AreEqual(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.Range.Fields[1].GetFieldCode());

    // Bu girdi, "A" dan farklı bir türe sahip olduğu için tablodan çıkarılacaktır.
    InsertTocEntry(builder, "TC field 3", "B", "1");

    // Bu giriş, 1-3 aralığının dışında bir giriş düzeyine sahip olduğu için tablodan çıkarılacaktır.
    InsertTocEntry(builder, "TC field 4", "A", "5");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TC.docx");

/// <summary>
/// Bir TC alanı eklemek için bir belge oluşturucu kullanın.
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
* ad alanı [Aspose.Words.Fields](../../fieldtoc/)
* toplantı [Aspose.Words](../../../)


