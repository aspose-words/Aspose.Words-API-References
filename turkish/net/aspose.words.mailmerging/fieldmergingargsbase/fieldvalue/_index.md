---
title: FieldMergingArgsBase.FieldValue
second_title: Aspose.Words for .NET API Referansı
description: FieldMergingArgsBase mülk. Veri kaynağından alanın değerini alır veya ayarlar.
type: docs
weight: 50
url: /tr/net/aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/
---
## FieldMergingArgsBase.FieldValue property

Veri kaynağından alanın değerini alır veya ayarlar.

```csharp
public object FieldValue { get; set; }
```

### Notlar

Bu özellik, adres mektup birleştirme motoru tarafından bu alan için veri kaynağınızdan az önce seçilen bir değer içeriyor. Özelliği ayarlayarak da değeri değiştirebilirsiniz.

### Örnekler

Adres mektup birleştirme gerçekleşirken MERGEFIELD'lerin aldığı değerlerin nasıl düzenleneceğini gösterir.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Adres mektup birleştirme sırasında alacakları değerleri düzenleyecek biçim anahtarlarına sahip bazı MERGEFIELD'ler ekleyin.
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
/// Adres mektup birleştirme sırasında MERGEFIELD'lerin aldığı değerleri düzenler.
/// Bu geri çağırmanın değeri üzerinde etkili olabilmesi için MERGEFIELD adının bir ön eki olmalıdır.
/// </summary>
private class FieldValueMergingCallback : IFieldMergingCallback
{
    /// <summary>
    /// Adres mektup birleştirme verileri bir MERGEFIELD ile birleştirdiğinde çağrılır.
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
* ad alanı [Aspose.Words.MailMerging](../../fieldmergingargsbase/)
* toplantı [Aspose.Words](../../../)


