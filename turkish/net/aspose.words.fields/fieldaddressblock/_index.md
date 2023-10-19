---
title: FieldAddressBlock Class
linktitle: FieldAddressBlock
articleTitle: FieldAddressBlock
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.FieldAddressBlock sınıf. ADRESSBLOCK alanını uygular C#'da.
type: docs
weight: 1530
url: /tr/net/aspose.words.fields/fieldaddressblock/
---
## FieldAddressBlock class

ADRESSBLOCK alanını uygular.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Alanlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fields/) dokümantasyon makalesi.

```csharp
public class FieldAddressBlock : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldAddressBlock](fieldaddressblock/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [ExcludedCountryOrRegionName](../../aspose.words.fields/fieldaddressblock/excludedcountryorregionname/) { get; set; } | Hariç tutulan ülke/bölge adını alır veya ayarlar. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir alır[`FieldFormat`](../fieldformat/) Alanın formatlamasına yazılı erişim sağlayan nesne. |
| [FormatAddressOnCountryOrRegion](../../aspose.words.fields/fieldaddressblock/formataddressoncountryorregion/) { get; set; } | Adresin, POST*CODE (Universal Postal Union 2006) tarafından tanımlandığı şekilde alıcının ülkesine/bölgesine göre biçimlendirilip biçimlendirilmeyeceğini alır veya ayarlar. |
| [IncludeCountryOrRegionName](../../aspose.words.fields/fieldaddressblock/includecountryorregionname/) { get; set; } | Ülke/bölge adının eklenip eklenmeyeceğini alır veya ayarlar. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucu yeniden hesaplanmamalıdır). |
| [LanguageId](../../aspose.words.fields/fieldaddressblock/languageid/) { get; set; } | Adresi biçimlendirmek için kullanılan dil kimliğini alır veya ayarlar. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [NameAndAddressFormat](../../aspose.words.fields/fieldaddressblock/nameandaddressformat/) { get; set; } | Ad ve adres biçimini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. Olabilir`hükümsüz` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [GetFieldNames](../../aspose.words.fields/fieldaddressblock/getfieldnames/)() | Alan tarafından kullanılan adres-mektup birleştirme alan adlarının bir koleksiyonunu döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alanın hemen ardından bir düğüm döndürür. Alanın sonu, üst düğümünün son child 'si ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa şunu döndürür:`hükümsüz` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Alanın bağlantısını kaldırır. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |

## Notlar

Bir adres bloğunu temsil eder. Biradres bloğuhedef ülkenin gerektirdiği sırayla bir posta adresi için uygun bilgileri belirten bir metin bloğudur.

## Örnekler

Bir alan tarafından kullanılan adres-mektup birleştirme alan adlarının nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Field sample - ADDRESSBLOCK.docx");

string[] addressFieldsExpect =
{
    "Company", "First Name", "Middle Name", "Last Name", "Suffix", "Address 1", "City", "State",
    "Country or Region", "Postal Code"
};

FieldAddressBlock addressBlockField = (FieldAddressBlock) doc.Range.Fields[0];
string[] addressBlockFieldNames = addressBlockField.GetFieldNames();
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
