---
title: "Aspose::Words::Fields::FieldPrintDate sınıfı"
linktitle: "FieldPrintDate"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldPrintDate sınıfı. PRINTDATE alanını uygular. Daha fazla bilgi edinmek için C++'deki belge makalesini ziyaret edin."
type: docs
weight: 81000
url: /tr/cpp/aspose.words.fields/fieldprintdate/
---
## FieldPrintDate class


PRINTDATE alanını uygular. Daha fazla bilgi edinmek için [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldPrintDate : public Aspose::Words::Fields::Field,
                       public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                       public Aspose::Words::Fields::IFieldWithCalendar
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Görüntülenen alan sonucunu temsil eden metni alır. |
| [get_End](../field/get_end/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldEnd](../field/get_fieldend/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldStart](../field/get_fieldstart/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_Format](../field/get_format/)() | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../fieldformat/) nesnesi alır. |
| [get_IsDirty](../field/get_isdirty/)() | Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [get_IsLocked](../field/get_islocked/)() | Alan'ın kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır veya ayarlar. |
| [get_LocaleId](../field/get_localeid/)() | Alan'ın LCID'sini alır veya ayarlar. |
| [get_Result](../field/get_result/)() | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [get_Separator](../field/get_separator/)() | Alan ayırıcıyı temsil eden düğümü alır. **null** olabilir. |
| [get_Start](../field/get_start/)() const | Alan başlangıcını temsil eden düğümü alır. |
| virtual [get_Type](../field/get_type/)() const | Microsoft Word alan türünü alır. |
| [get_UseLunarCalendar](./get_uselunarcalendar/)() override | Hijri Ay takvimi veya İbrani Ay takvimini kullanıp kullanmayacağını alır veya ayarlar. |
| [get_UseSakaEraCalendar](./get_usesakaeracalendar/)() override | Saka Dönemi takvimini kullanıp kullanmayacağını alır veya ayarlar. |
| [get_UseUmAlQuraCalendar](./get_useumalquracalendar/)() override | Um-al-Qura takvimini kullanıp kullanmayacağını alır veya ayarlar. |
| [GetFieldCode](../field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Alanı belgeden kaldırır. Alanın hemen sonrasındaki bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafını döndürür. Alan zaten kaldırılmışsa, **null** döndürür. |
| [set_IsDirty](../field/set_isdirty/)(bool) | [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) için ayarlayıcı. |
| [set_IsLocked](../field/set_islocked/)(bool) | [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) için ayarlayıcı. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) için ayarlayıcı. |
| [set_Result](../field/set_result/)(const System::String\&) | [Aspose::Words::Fields::Field::get_Result](../field/get_result/) için ayarlayıcı. |
| [set_UseLunarCalendar](./set_uselunarcalendar/)(bool) | Ayarlayıcı [Aspose::Words::Fields::FieldPrintDate::get_UseLunarCalendar](./get_uselunarcalendar/). |
| [set_UseSakaEraCalendar](./set_usesakaeracalendar/)(bool) | Ayarlayıcı [Aspose::Words::Fields::FieldPrintDate::get_UseSakaEraCalendar](./get_usesakaeracalendar/). |
| [set_UseUmAlQuraCalendar](./set_useumalquracalendar/)(bool) | Ayarlayıcı [Aspose::Words::Fields::FieldPrintDate::get_UseUmAlQuraCalendar](./get_useumalquracalendar/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Alan bağlantısını kaldırır. |
| [Update](../field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
| [Update](../field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |

## Örnekler



Okunan PRINTDATE alanlarını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - PRINTDATE.docx");

// Bir belge bir yazıcıyla yazdırıldığında veya PDF olarak yazdırıldığında (ancak PDF olarak dışa aktarılmadığında),
// PRINTDATE alanları yazdırma işleminin tarih/saatini gösterecektir.
// Yazdırma gerçekleşmemişse, bu alanlar "0/0/0000" gösterecektir.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(0));

ASSERT_EQ(u"3/25/2020 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE ", field->GetFieldCode());

// Aşağıda PRINTDATE alanının göreli olarak kullanabileceği üç farklı takvim türü bulunmaktadır
// son yazdırma işleminin tarih ve saatini gösterebilir.
// 1 -  İslami Ay Takvimi:
field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(1));

ASSERT_TRUE(field->get_UseLunarCalendar());
ASSERT_EQ(u"8/1/1441 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\h", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(2));

// 2 -  Umm al-Qura takvimi:
ASSERT_TRUE(field->get_UseUmAlQuraCalendar());
ASSERT_EQ(u"8/1/1441 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\u", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(3));

// 3 -  Hint Ulusal Takvimi:
ASSERT_TRUE(field->get_UseSakaEraCalendar());
ASSERT_EQ(u"1/5/1942 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\s", field->GetFieldCode());
```

## Ayrıca Bakınız

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
