---
title: FieldMergingArgsBase.FieldValue
linktitle: FieldValue
articleTitle: FieldValue
second_title: Aspose.Words for .NET
description: FieldMergingArgsBase FieldValue mülk. Alanın değerini veri kaynağından alır veya ayarlar C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/
---
## FieldMergingArgsBase.FieldValue property

Alanın değerini veri kaynağından alır veya ayarlar.

```csharp
public object FieldValue { get; set; }
```

## Notlar

Bu özellik, adres-mektup birleştirme motoru tarafından bu alan için veri kaynağınızdan seçilen bir değeri içerir. Ayrıca özelliği ayarlayarak değeri değiştirebilirsiniz.

## Örnekler

Adres-mektup birleştirme gerçekleşirken MERGEFIELD'lerin aldığı değerlerin nasıl düzenleneceğini gösterir.

```csharp
public void FieldFormats()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Adres-mektup birleştirme sırasında alacakları değerleri düzenleyecek format anahtarlarına sahip bazı MERGEFIELD'leri ekleyin.
    builder.InsertField("MERGEFIELD text_Field1 \\* Caps", null);
    builder.Write(", ");
    builder.InsertField("MERGEFIELD text_Field2 \\* Upper", null);
    builder.Write(", ");
    builder.InsertField("MERGEFIELD numeric_Field1 \\# 0.0", null);

    builder.Document.MailMerge.FieldMergingCallback = new FieldValueMergingCallback();

    builder.Document.MailMerge.Execute(
        new string[] { "text_Field1", "text_Field2", "numeric_Field1" },
        new object[] { "Field 1", "Field 2", 10 });
    string t = doc.GetText().Trim();
    Assert.AreEqual("Merge Value For \"Text_Field1\": Field 1, MERGE VALUE FOR \"TEXT_FIELD2\": FIELD 2, 10000.0", doc.GetText().Trim());
}

/// <summary>
/// Adres-mektup birleştirme sırasında MERGEFIELD'lerin aldığı değerleri düzenler.
/// Bu geri çağırmanın değerini etkilemesi için MERGEFIELD adının bir öneki olması gerekir.
/// </summary>
private class FieldValueMergingCallback : IFieldMergingCallback
{
    /// <summary>
    /// Adres-mektup birleştirme verileri MERGEFIELD ile birleştirdiğinde çağrılır.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs e)
    {
        if (e.FieldName.StartsWith("text_"))
            e.FieldValue = $"Merge value for \"{e.FieldName}\": {(string)e.FieldValue}";
        else if (e.FieldName.StartsWith("numeric_"))
            e.FieldValue = (int)e.FieldValue * 1000;
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        // Hiçbir şey yapma.
    }
}
```

### Ayrıca bakınız

* class [FieldMergingArgsBase](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
