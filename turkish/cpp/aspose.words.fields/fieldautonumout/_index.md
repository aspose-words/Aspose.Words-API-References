---
title: "Aspose::Words::Fields::FieldAutoNumOut sınıfı"
linktitle: "FieldAutoNumOut"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldAutoNumOut sınıfı. AUTONUMOUT alanını uygular. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 14000
url: /tr/cpp/aspose.words.fields/fieldautonumout/
---
## FieldAutoNumOut class


AUTONUMOUT alanını uygular. Daha fazla bilgi edinmek için [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldAutoNumOut : public Aspose::Words::Fields::Field
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
| [GetFieldCode](../field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Alanı belgeden kaldırır. Alanın hemen sonrasındaki bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafını döndürür. Alan zaten kaldırılmışsa, **null** döndürür. |
| [set_IsDirty](../field/set_isdirty/)(bool) | [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) için ayarlayıcı. |
| [set_IsLocked](../field/set_islocked/)(bool) | [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) için ayarlayıcı. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) için ayarlayıcı. |
| [set_Result](../field/set_result/)(const System::String\&) | [Aspose::Words::Fields::Field::get_Result](../field/get_result/) için ayarlayıcı. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Alan bağlantısını kaldırır. |
| [Update](../field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
| [Update](../field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |

## Örnekler



AUTONUMOUT alanlarını kullanarak paragrafları nasıl numaralandıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// AUTONUMOUT alanları, her AUTONUMOUT alanında artan bir sayı gösterir.
// AUTONUM alanlarının aksine, AUTONUMOUT alanları taslak numaralandırma şemasını kullanır,
// bunu Microsoft Word'de Biçim -> Madde İşaretleri ve Numaralandırma -> "Outline Numbered" aracılığıyla tanımlayabiliriz.
// Bu, numaralı bir liste gibi öğeleri otomatik olarak numaralandırmamıza olanak tanır.
// LISTNUM alanları, AUTONUMOUT alanlarına yeni bir alternatiftir.
// Bu alan "1." görüntüler.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoNumOutline, true);
builder->Writeln(u"\tParagraph 1.");

// Bu alan "2." görüntüler.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoNumOutline, true);
builder->Writeln(u"\tParagraph 2.");

for (auto&& field : System::IterateOver<Aspose::Words::Fields::FieldAutoNumOut>(doc->get_Range()->get_Fields()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fields::Field>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fields::Field> f)>>([](System::SharedPtr<Aspose::Words::Fields::Field> f) -> bool
{
    return f->get_Type() == Aspose::Words::Fields::FieldType::FieldAutoNumOutline;
})))->LINQ_ToList()))
{
    ASSERT_EQ(u" AUTONUMOUT ", field->GetFieldCode());
}

doc->Save(get_ArtifactsDir() + u"Field.AUTONUMOUT.docx");
```

## Ayrıca Bakınız

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
