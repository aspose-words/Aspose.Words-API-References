---
title: FieldTC.TypeIdentifier
second_title: Aspose.Words for .NET API Referansı
description: FieldTC mülk. Bu alan için bir tür tanımlayıcısı alır veya ayarlar bu genellikle bir harftir.
type: docs
weight: 50
url: /tr/net/aspose.words.fields/fieldtc/typeidentifier/
---
## FieldTC.TypeIdentifier property

Bu alan için bir tür tanımlayıcısı alır veya ayarlar (bu genellikle bir harftir).

```csharp
public string TypeIdentifier { get; set; }
```

### Örnekler

TOC alanının nasıl ekleneceğini ve hangi TC alanlarının giriş olarak sonuçlanacağını filtreleyeceğini gösterir.

```csharp
public void FieldTocEntryIdentifier()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Tüm TC alanlarını bir içindekiler tablosunda derleyecek bir TOC alanı ekleyin.
    FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Alanı yalnızca "A" tipindeki TC girişlerini ve 1 ile 3 arasındaki giriş seviyesini alacak şekilde yapılandırın.
    fieldToc.EntryIdentifier = "A";
    fieldToc.EntryLevelRange = "1-3";

    Assert.AreEqual(" TOC  \\f A \\l 1-3", fieldToc.GetFieldCode());

    // Bu iki giriş tabloda görünecektir.
    builder.InsertBreak(BreakType.PageBreak);
    InsertTocEntry(builder, "TC field 1", "A", "1");
    InsertTocEntry(builder, "TC field 2", "A", "2");

    Assert.AreEqual(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.Range.Fields[1].GetFieldCode());

    // Bu girdi "A"dan farklı bir türe sahip olduğundan tablodan çıkarılacaktır.
    InsertTocEntry(builder, "TC field 3", "B", "1");

    // Bu giriş, 1-3 aralığının dışında bir giriş düzeyine sahip olduğundan tablodan çıkarılacaktır.
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

* class [FieldTC](../)
* ad alanı [Aspose.Words.Fields](../../fieldtc/)
* toplantı [Aspose.Words](../../../)


