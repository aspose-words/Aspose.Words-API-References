---
title: FieldFillIn.PromptText
linktitle: PromptText
articleTitle: PromptText
second_title: .NET için Aspose.Words
description: FieldFillIn PromptText özelliğini keşfedin, kullanıcı deneyimini geliştirmek ve arayüz anlaşılırlığını artırmak için istem penceresi başlıklarını kolayca özelleştirin.
type: docs
weight: 40
url: /tr/net/aspose.words.fields/fieldfillin/prompttext/
---
## FieldFillIn.PromptText property

İstem metnini (istem penceresinin başlığı) alır veya ayarlar.

```csharp
public string PromptText { get; set; }
```

## Örnekler

FILLIN alanının kullanıcıdan yanıt istemek için nasıl kullanılacağını gösterir.

```csharp
public void FieldFillIn()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Bir FILLIN alanı ekleyin. Bu alanı Microsoft Word'de manuel olarak güncellediğimizde,
    // bize bir yanıt girmemizi isteyecektir. Alan daha sonra yanıtı metin olarak gösterecektir.
    FieldFillIn field = (FieldFillIn)builder.InsertField(FieldType.FieldFillIn, true);
    field.PromptText = "Please enter a response:";
    field.DefaultResponse = "A default response.";

    // Ayrıca bu alanları, kullanıcıdan her sayfa için benzersiz bir yanıt istemek için de kullanabiliriz
    // Microsoft Word kullanılarak yapılan bir posta birleştirme sırasında oluşturuldu.
    field.PromptOnceOnMailMerge = true;

    Assert.AreEqual(" FILLIN  \"Please enter a response:\" \\d \"A default response.\" \\o", field.GetFieldCode());

    FieldMergeField mergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    mergeField.FieldName = "MergeField";

    // Eğer bir posta birleştirme işlemini programatik olarak gerçekleştirirsek, özel bir istem yanıtlayıcısı kullanabiliriz
    // posta birleştirme işleminin karşılaştığı FILLIN alanları için yanıtları otomatik olarak düzenlemek için.
    doc.FieldOptions.UserPromptRespondent = new PromptRespondent();
    doc.MailMerge.Execute(new [] { "MergeField" }, new object[] { "" });

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.FILLIN.docx");
}

/// <summary>
/// Bir posta birleştirme sırasında her FILLIN alanının varsayılan yanıtına bir satır ekler.
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
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
