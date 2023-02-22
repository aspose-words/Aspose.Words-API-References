---
title: Class FieldFillIn
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fields.FieldFillIn sınıf. DOLDURMA alanını uygular.
type: docs
weight: 1740
url: /tr/net/aspose.words.fields/fieldfillin/
---
## FieldFillIn class

DOLDURMA alanını uygular.

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
| [DefaultResponse](../../aspose.words.fields/fieldfillin/defaultresponse/) { get; set; } | Varsayılan kullanıcı yanıtını alır veya ayarlar (istem penceresinde bulunan ilk değer). |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | [`FieldFormat`](../fieldformat/) alanın biçimlendirmesine yazılı erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [PromptOnceOnMailMerge](../../aspose.words.fields/fieldfillin/promptonceonmailmerge/) { get; set; } | Bir adres mektup birleştirme işlemi başına kullanıcı yanıtının bir kez alınıp alınmayacağını alır veya ayarlar. |
| [PromptText](../../aspose.words.fields/fieldfillin/prompttext/) { get; set; } | Bilgi istemi metnini alır veya ayarlar (bilgi istemi penceresinin başlığı). |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. null. olabilir |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alandan hemen sonra bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğu ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa, döner **hükümsüz** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Bağlantıyı kaldır alanını gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |

### Notlar

Kullanıcıdan metin girmesini ister.

### Örnekler

Kullanıcıdan bir yanıt istemek için DOLDURMA alanının nasıl kullanılacağını gösterir.

```csharp
public void FieldFillIn()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Bir FILLIN alanı ekleyin. Bu alanı Microsoft Word'de manuel olarak güncellediğimizde,
    // bir yanıt girmemizi isteyecek. Alan daha sonra yanıtı metin olarak görüntüler.
    FieldFillIn field = (FieldFillIn)builder.InsertField(FieldType.FieldFillIn, true);
    field.PromptText = "Please enter a response:";
    field.DefaultResponse = "A default response.";

    // Bu alanları, kullanıcıdan her sayfa için benzersiz bir yanıt istemek için de kullanabiliriz.
    // Microsoft Word kullanılarak yapılan adres mektup birleştirme sırasında oluşturuldu.
    field.PromptOnceOnMailMerge = true;

    Assert.AreEqual(" FILLIN  \"Please enter a response:\" \\d \"A default response.\" \\o", field.GetFieldCode());

    FieldMergeField mergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    mergeField.FieldName = "MergeField";

    // Programlı olarak adres mektup birleştirme gerçekleştirirsek, özel bir istem yanıtlayıcı kullanabiliriz
    // adres mektup birleştirmenin karşılaştığı FILLIN alanlarına yönelik yanıtları otomatik olarak düzenlemek için.
    doc.FieldOptions.UserPromptRespondent = new PromptRespondent();
    doc.MailMerge.Execute(new [] { "MergeField" }, new object[] { "" });

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.FILLIN.docx");

/// <summary>
/// Adres mektup birleştirme sırasında her FILLIN alanının varsayılan yanıtının başına bir satır ekler.
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


