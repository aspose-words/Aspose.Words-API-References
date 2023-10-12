---
title: FieldOptions.UserPromptRespondent
second_title: Aspose.Words for .NET API Referansı
description: FieldOptions mülk. Alan güncellemesi sırasında kullanıcı istemlerine yanıt vereni alır veya ayarlar.
type: docs
weight: 220
url: /tr/net/aspose.words.fields/fieldoptions/userpromptrespondent/
---
## FieldOptions.UserPromptRespondent property

Alan güncellemesi sırasında kullanıcı istemlerine yanıt vereni alır veya ayarlar.

```csharp
public IFieldUserPromptRespondent UserPromptRespondent { get; set; }
```

### Notlar

Bu özelliğin değeri şu şekilde ayarlanmışsa`hükümsüz` , istem 'de kullanıcı yanıtı gerektiren alanlar (örneğin[`FieldAsk`](../../fieldask/) veya[`FieldFillIn`](../../fieldfillin/)) güncellenmez.

Varsayılan değer:`hükümsüz`.

### Örnekler

ASK alanının nasıl oluşturulacağını ve özelliklerinin nasıl ayarlanacağını gösterir.

```csharp
public void FieldAsk()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // ASK alanımıza verilecek yanıtın yerleştirileceği alanı yerleştirin.
    FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    fieldRef.BookmarkName = "MyAskField";
    builder.Writeln();

    Assert.AreEqual(" REF  MyAskField", fieldRef.GetFieldCode());

    // ASK alanını ekleyin ve REF alanımıza yer işareti adıyla referans verecek şekilde özelliklerini düzenleyin.
    FieldAsk fieldAsk = (FieldAsk)builder.InsertField(FieldType.FieldAsk, true);
    fieldAsk.BookmarkName = "MyAskField";
    fieldAsk.PromptText = "Please provide a response for this ASK field";
    fieldAsk.DefaultResponse = "Response from within the field.";
    fieldAsk.PromptOnceOnMailMerge = true;
    builder.Writeln();

    Assert.AreEqual(
        " ASK  MyAskField \"Please provide a response for this ASK field\" \\d \"Response from within the field.\" \\o",
        fieldAsk.GetFieldCode());

    // ASK alanları, adres-mektup birleştirme sırasında ilgili REF alanlarına varsayılan yanıtı uygular.
    DataTable table = new DataTable("My Table");
    table.Columns.Add("Column 1");
    table.Rows.Add("Row 1");
    table.Rows.Add("Row 2");

    FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    fieldMergeField.FieldName = "Column 1";

    // Özel bir istem yanıtlayıcı ile ASK alanlarımızdaki varsayılan yanıtı değiştirebilir veya geçersiz kılabiliriz,
    // adres-mektup birleştirme sırasında gerçekleşecek.
    doc.FieldOptions.UserPromptRespondent = new MyPromptRespondent();
    doc.MailMerge.Execute(table);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.ASK.docx");
}

/// <summary>
/// Adres-mektup birleştirme sırasında ASK alanının varsayılan yanıtının başına metin ekler.
/// </summary>
private class MyPromptRespondent : IFieldUserPromptRespondent
{
    public string Respond(string promptText, string defaultResponse)
    {
        return "Response from MyPromptRespondent. " + defaultResponse;
    }
}
```

### Ayrıca bakınız

* interface [IFieldUserPromptRespondent](../../ifielduserpromptrespondent/)
* class [FieldOptions](../)
* ad alanı [Aspose.Words.Fields](../../fieldoptions/)
* toplantı [Aspose.Words](../../../)


