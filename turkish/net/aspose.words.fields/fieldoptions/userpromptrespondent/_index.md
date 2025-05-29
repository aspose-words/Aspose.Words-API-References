---
title: FieldOptions.UserPromptRespondent
linktitle: UserPromptRespondent
articleTitle: UserPromptRespondent
second_title: .NET için Aspose.Words
description: FieldOptions UserPromptRespondent özelliğinin, alan güncellemeleri sırasında yanıtlayan etkileşimlerini yöneterek kullanıcı deneyimini nasıl geliştirdiğini keşfedin.
type: docs
weight: 220
url: /tr/net/aspose.words.fields/fieldoptions/userpromptrespondent/
---
## FieldOptions.UserPromptRespondent property

Alan güncellemesi sırasında yanıtlayanı kullanıcı istemlerine göre alır veya ayarlar.

```csharp
public IFieldUserPromptRespondent UserPromptRespondent { get; set; }
```

## Notlar

Bu özelliğin değeri şu şekilde ayarlanırsa:`hükümsüz` , prompting (örneğin) kullanıcı yanıtını gerektiren alanlar[`FieldAsk`](../../fieldask/) veya[`FieldFillIn`](../../fieldfillin/)) güncellenmiyor.

Varsayılan değer:`hükümsüz`.

## Örnekler

ASK alanının nasıl oluşturulacağını ve özelliklerinin nasıl ayarlanacağını gösterir.

```csharp
public void FieldAsk()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // ASK alanımıza verilecek cevabın yer alacağı bir alan yerleştiriyoruz.
    FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    fieldRef.BookmarkName = "MyAskField";
    builder.Writeln();

    Assert.AreEqual(" REF  MyAskField", fieldRef.GetFieldCode());

    // ASK alanını ekleyin ve özelliklerini düzenleyerek yer imi adına göre REF alanımıza başvuralım.
    FieldAsk fieldAsk = (FieldAsk)builder.InsertField(FieldType.FieldAsk, true);
    fieldAsk.BookmarkName = "MyAskField";
    fieldAsk.PromptText = "Please provide a response for this ASK field";
    fieldAsk.DefaultResponse = "Response from within the field.";
    fieldAsk.PromptOnceOnMailMerge = true;
    builder.Writeln();

    Assert.AreEqual(
        " ASK  MyAskField \"Please provide a response for this ASK field\" \\d \"Response from within the field.\" \\o",
        fieldAsk.GetFieldCode());

    // ASK alanları, bir posta birleştirme sırasında ilgili REF alanlarına varsayılan yanıtı uygular.
    DataTable table = new DataTable("My Table");
    table.Columns.Add("Column 1");
    table.Rows.Add("Row 1");
    table.Rows.Add("Row 2");

    FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    fieldMergeField.FieldName = "Column 1";

    // ASK alanlarımızdaki varsayılan yanıtı özel bir istem yanıtlayıcısıyla değiştirebilir veya geçersiz kılabiliriz.
    // posta birleştirme sırasında gerçekleşecektir.
    doc.FieldOptions.UserPromptRespondent = new MyPromptRespondent();
    doc.MailMerge.Execute(table);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.ASK.docx");
}

/// <summary>
/// Bir posta birleştirme sırasında ASK alanının varsayılan yanıtına metin ekler.
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
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
