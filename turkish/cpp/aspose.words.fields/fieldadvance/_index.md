---
title: "Aspose::Words::Fields::FieldAdvance sınıfı"
linktitle: "FieldAdvance"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldAdvance sınıfı. ADVANCE alanını uygular. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.fields/fieldadvance/
---
## FieldAdvance class


ADVANCE alanını uygular. Daha fazla bilgi için [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldAdvance : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Görüntülenen alan sonucunu temsil eden metni alır. |
| [get_DownOffset](./get_downoffset/)() | Alanı izleyen metnin aşağı doğru hareket ettirilmesi gereken puan sayısını alır veya ayarlar. |
| [get_End](../field/get_end/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldEnd](../field/get_fieldend/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldStart](../field/get_fieldstart/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_Format](../field/get_format/)() | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../fieldformat/) nesnesi alır. |
| [get_HorizontalPosition](./get_horizontalposition/)() | Alanı izleyen metnin sütunun, çerçevenin veya metin kutusunun sol kenarından yatay olarak hareket ettirilmesi gereken puan sayısını alır veya ayarlar. |
| [get_IsDirty](../field/get_isdirty/)() | Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [get_IsLocked](../field/get_islocked/)() | Alan'ın kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır veya ayarlar. |
| [get_LeftOffset](./get_leftoffset/)() | Alanı izleyen metnin sola hareket ettirilmesi gereken puan sayısını alır veya ayarlar. |
| [get_LocaleId](../field/get_localeid/)() | Alan'ın LCID'sini alır veya ayarlar. |
| [get_Result](../field/get_result/)() | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [get_RightOffset](./get_rightoffset/)() | Alanı izleyen metnin sağa hareket ettirilmesi gereken puan sayısını alır veya ayarlar. |
| [get_Separator](../field/get_separator/)() | Alan ayırıcıyı temsil eden düğümü alır. **null** olabilir. |
| [get_Start](../field/get_start/)() const | Alan başlangıcını temsil eden düğümü alır. |
| virtual [get_Type](../field/get_type/)() const | Microsoft Word alan türünü alır. |
| [get_UpOffset](./get_upoffset/)() | Alanı izleyen metnin yukarı doğru hareket ettirilmesi gereken puan sayısını alır veya ayarlar. |
| [get_VerticalPosition](./get_verticalposition/)() | Alanı izleyen metnin sayfanın üst kenarından dikey olarak hareket ettirilmesi gereken puan sayısını alır veya ayarlar. |
| [GetFieldCode](../field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Alanı belgeden kaldırır. Alanın hemen sonrasındaki bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafını döndürür. Alan zaten kaldırılmışsa, **null** döndürür. |
| [set_DownOffset](./set_downoffset/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldAdvance::get_DownOffset](./get_downoffset/). |
| [set_HorizontalPosition](./set_horizontalposition/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldAdvance::get_HorizontalPosition](./get_horizontalposition/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) için ayarlayıcı. |
| [set_IsLocked](../field/set_islocked/)(bool) | [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) için ayarlayıcı. |
| [set_LeftOffset](./set_leftoffset/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldAdvance::get_LeftOffset](./get_leftoffset/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) için ayarlayıcı. |
| [set_Result](../field/set_result/)(const System::String\&) | [Aspose::Words::Fields::Field::get_Result](../field/get_result/) için ayarlayıcı. |
| [set_RightOffset](./set_rightoffset/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldAdvance::get_RightOffset](./get_rightoffset/). |
| [set_UpOffset](./set_upoffset/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldAdvance::get_UpOffset](./get_upoffset/). |
| [set_VerticalPosition](./set_verticalposition/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldAdvance::get_VerticalPosition](./get_verticalposition/) için. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Alan bağlantısını kaldırır. |
| [Update](../field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
| [Update](../field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |

## Örnekler



Bir ADVANCE alanı eklemeyi ve özelliklerini düzenlemeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This text is in its normal place.");

// Aşağıda, ADVANCE alanını kullanarak ardından gelen metnin konumunu ayarlamanın iki yolu verilmiştir.
// Bir ADVANCE alanının etkileri paragraf sonuna kadar uygulanmaya devam eder,
// veya başka bir ADVANCE alanı ofset/koordinat değerlerini günceller.
// 1 -  Yönsel bir ofset belirtin:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_RightOffset(u"5");
field->set_UpOffset(u"5");

ASSERT_EQ(u" ADVANCE  \\r 5 \\u 5", field->GetFieldCode());

builder->Write(u"This text will be moved up and to the right.");

field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_DownOffset(u"5");
field->set_LeftOffset(u"100");

ASSERT_EQ(u" ADVANCE  \\d 5 \\l 100", field->GetFieldCode());

builder->Writeln(u"This text is moved down and to the left, overlapping the previous text.");

// 2 -  Metni koordinatlarla belirtilen bir konuma taşıyın:
field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_HorizontalPosition(u"-100");
field->set_VerticalPosition(u"200");

ASSERT_EQ(u" ADVANCE  \\x -100 \\y 200", field->GetFieldCode());

builder->Write(u"This text is in a custom position.");

doc->Save(get_ArtifactsDir() + u"Field.ADVANCE.docx");
```

## Ayrıca Bakınız

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
