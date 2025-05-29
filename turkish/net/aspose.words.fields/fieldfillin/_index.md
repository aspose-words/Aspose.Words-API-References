---
title: FieldFillIn Class
linktitle: FieldFillIn
articleTitle: FieldFillIn
second_title: .NET için Aspose.Words
description: FILLIN alanlarını kolayca uygulamak, belge otomasyonunuzu ve kullanıcı etkileşiminizi geliştirmek için Aspose.Words.Fields.FieldFillIn sınıfını keşfedin.
type: docs
weight: 2300
url: /tr/net/aspose.words.fields/fieldfillin/
---
## FieldFillIn class

FILLIN alanını uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class FieldFillIn : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldFillIn](fieldfillin/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DefaultResponse](../../aspose.words.fields/fieldfillin/defaultresponse/) { get; set; } | Varsayılan kullanıcı yanıtını alır veya ayarlar (istem penceresinde bulunan başlangıç değeri). |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir tane alır[`FieldFormat`](../fieldformat/)alanın biçimlendirmesine yazılmış erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [PromptOnceOnMailMerge](../../aspose.words.fields/fieldfillin/promptonceonmailmerge/) { get; set; } | Kullanıcı yanıtının bir posta birleştirme işlemi başına bir kez alınıp alınmayacağını alır veya ayarlar. |
| [PromptText](../../aspose.words.fields/fieldfillin/prompttext/) { get; set; } | İstem metnini (istem penceresinin başlığı) alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcısı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcısını temsil eden düğümü alır.`hükümsüz` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alanın hemen ardından bir düğüm döndürür. Alanın sonu, üst düğümünün son alt 'siyse, üst paragrafını döndürür. Alan zaten kaldırılmışsa, şunu döndürür`hükümsüz` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Alan bağlantısını kaldırma işlemini gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |

## Notlar

Kullanıcıdan metin girmesini ister.

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

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
