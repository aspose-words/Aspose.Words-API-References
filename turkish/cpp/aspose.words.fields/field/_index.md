---
title: "Aspose::Words::Fields::Field sınıfı"
linktitle: "Alan"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::Field sınıfı. Bir Microsoft Word belge alanını temsil eder. Daha fazla bilgi için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.fields/field/
---
## Field class


Bir Microsoft Word belge alanını temsil eder. Daha fazla bilgi için dokümantasyon makalesini ziyaret edin.

```cpp
class Field : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_DisplayResult](./get_displayresult/)() | Görüntülenen alan sonucunu temsil eden metni alır. |
| [get_End](./get_end/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldEnd](./get_fieldend/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldStart](./get_fieldstart/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_Format](./get_format/)() | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../fieldformat/) nesnesi alır. |
| [get_IsDirty](./get_isdirty/)() | Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [get_IsLocked](./get_islocked/)() | Alan'ın kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır veya ayarlar. |
| [get_LocaleId](./get_localeid/)() | Alan'ın LCID'sini alır veya ayarlar. |
| [get_Result](./get_result/)() | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [get_Separator](./get_separator/)() | Alan ayırıcıyı temsil eden düğümü alır. **null** olabilir. |
| [get_Start](./get_start/)() const | Alan başlangıcını temsil eden düğümü alır. |
| virtual [get_Type](./get_type/)() const | Microsoft Word alan türünü alır. |
| [GetFieldCode](./getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](./getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](./remove/)() | Alanı belgeden kaldırır. Alanın hemen sonrasındaki bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafını döndürür. Alan zaten kaldırılmışsa, **null** döndürür. |
| [set_IsDirty](./set_isdirty/)(bool) | Ayarlayıcı [Aspose::Words::Fields::Field::get_IsDirty](./get_isdirty/) için. |
| [set_IsLocked](./set_islocked/)(bool) | Ayarlayıcı [Aspose::Words::Fields::Field::get_IsLocked](./get_islocked/) için. |
| [set_LocaleId](./set_localeid/)(int32_t) | Ayarlayıcı [Aspose::Words::Fields::Field::get_LocaleId](./get_localeid/) için. |
| [set_Result](./set_result/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::Field::get_Result](./get_result/) için. |
| static [Type](./type/)() |  |
| [Unlink](./unlink/)() | Alan bağlantısını kaldırır. |
| [Update](./update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
| [Update](./update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
## Açıklamalar


Word belgesindeki bir alan, alan başlangıcı, alan kodu, alan ayırıcı, alan sonucu ve alan sonu dahil olmak üzere birden çok düğümden oluşan karmaşık bir yapıdır. [Fields](../) iç içe yer alabilir, zengin içerik içerebilir ve bir belgede birden çok paragraf veya bölümü kapsayabilir. [Field](./) sınıfı, bir alanla tek bir nesne gibi çalışmayı sağlayan özellikler ve yöntemler sunan bir \"fasad\" nesnedir.

Bu [Start](./get_start/), [Separator](./get_separator/) ve [End](./get_end/) özellikleri, sırasıyla alanın başlangıç, ayırıcı ve son düğümlerine işaret eder.

Alan başlangıcı ile ayırıcı arasındaki içerik alan kodudur. Alan ayırıcı ile alan sonu arasındaki içerik alan sonucudur. Alan kodu genellikle talimatları belirten bir veya daha fazla [Run](../../aspose.words/run/) nesnesinden oluşur. İşleme uygulamasının, alan sonucunu hesaplamak için alan kodunu çalıştırması beklenir.

Alan sonuçlarını hesaplama sürecine alan güncellemesi denir. Aspose.Words, çoğu alan tipinin sonuçlarını Microsoft Word'ün yaptığı aynı şekilde güncelleyebilir. Özellikle, Aspose.Words en karmaşık formül alanlarının bile sonuçlarını hesaplayabilir. Tek bir alanın sonucunu hesaplamak için [Update](./update/) metodunu kullanın. Tüm belgede alanları güncellemek için [UpdateFields](../../aspose.words/document/updatefields/) metodunu kullanın.

Alan kodunun düz metin sürümünü [GetFieldCode()](./getfieldcode/) metodunu kullanarak alabilirsiniz. Alan sonucunun düz metin sürümünü [Result](./get_result/) özelliği ile alıp ayarlayabilirsiniz. Hem alan kodu hem de alan sonucu, iç içe alanlar, paragraflar, şekiller, tablolar gibi karmaşık içerikler içerebilir; bu durumda daha fazla kontrol gerekirse alan düğümleriyle doğrudan çalışmak isteyebilirsiniz.

Doğrudan [Field](./) sınıfının örneklerini oluşturmazsınız. Yeni bir alan oluşturmak için [InsertField()](../) yöntemini kullanın.

## Örnekler



Bir alan kodu kullanarak bir belgeye alan eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// InsertField yönteminin bu aşırı yüklemesi, eklenen alanları otomatik olarak günceller.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
