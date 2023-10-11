---
title: FieldFillIn.DefaultResponse
second_title: Aspose.Words for .NET API Referansı
description: FieldFillIn mülk. Varsayılan kullanıcı yanıtını alır veya ayarlar bilgi istemi penceresinde yer alan başlangıç değeri.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldfillin/defaultresponse/
---
## FieldFillIn.DefaultResponse property

Varsayılan kullanıcı yanıtını alır veya ayarlar (bilgi istemi penceresinde yer alan başlangıç değeri).

```csharp
public string DefaultResponse { get; set; }
```

### Örnekler

Kullanıcıdan yanıt istemek için FILLIN alanının nasıl kullanılacağını gösterir.

```csharp
public void FieldFillIn()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Bir FILLIN alanı ekleyin. Bu alanı Microsoft Word'de manuel olarak güncellediğimizde,
    // bizden bir yanıt girmemizi isteyecek. Alan daha sonra yanıtı metin olarak görüntüleyecektir.
    FieldFillIn field = (FieldFillIn)builder.InsertField(FieldType.FieldFillIn, true);
    field.PromptText = "Please enter a response:";
    field.DefaultResponse = "A default response.";

    // Bu alanları kullanıcıdan her sayfa için benzersiz bir yanıt istemek amacıyla da kullanabiliriz
    // Microsoft Word kullanılarak yapılan adres-mektup birleştirme sırasında oluşturuldu.
    field.PromptOnceOnMailMerge = true;

    Assert.AreEqual(" FILLIN  \"Please enter a response:\" \\d \"A default response.\" \\o", field.GetFieldCode());

    FieldMergeField mergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    mergeField.FieldName = "MergeField";

    // Adres-mektup birleştirmeyi programlı olarak gerçekleştirirsek, özel bir istem yanıtlayıcısı kullanabiliriz
    // Adres-mektup birleştirmenin karşılaştığı FILLIN alanlarına yönelik yanıtları otomatik olarak düzenlemek için.
    doc.FieldOptions.UserPromptRespondent = new PromptRespondent();
    doc.MailMerge.Execute(new [] { "MergeField" }, new object[] { "" });

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.FILLIN.docx");
}

/// <summary>
/// Adres-mektup birleştirme sırasında her FILLIN alanının varsayılan yanıtının başına bir satır eklenir.
/// </summary>
private class PromptRespondent : IFieldUserPromptRespondent
{
    public string Respond(string promptText, string defaultResponse)
    {
        return "Response modified by PromptRespondent. " + defaultResponse;
    }
}
```

### Ayrıca bakınız

* class [FieldFillIn](../)
* ad alanı [Aspose.Words.Fields](../../fieldfillin/)
* toplantı [Aspose.Words](../../../)


