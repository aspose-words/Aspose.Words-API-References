---
title: "Aspose::Words::Fields::FieldInclude class"
linktitle: "FieldInclude"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldInclude sınıfı. INCLUDE alanını uygular. Daha fazla bilgi için C++'daki  dokümantasyon makalesini ziyaret edin."
type: docs
weight: 56000
url: /tr/cpp/aspose.words.fields/fieldinclude/
---
## FieldInclude class


INCLUDE alanını uygular. Daha fazla bilgi edinmek için, [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldInclude : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                     public Aspose::Words::Fields::IFieldIncludeTextCode
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() override | Belgeye dahil edilecek yer iminin adını alır veya ayarlar. |
| [get_DisplayResult](../field/get_displayresult/)() | Görüntülenen alan sonucunu temsil eden metni alır. |
| [get_End](../field/get_end/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldEnd](../field/get_fieldend/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldStart](../field/get_fieldstart/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_Format](../field/get_format/)() | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../fieldformat/) nesnesi alır. |
| [get_IsDirty](../field/get_isdirty/)() | Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [get_IsLocked](../field/get_islocked/)() | Alan'ın kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır veya ayarlar. |
| [get_LocaleId](../field/get_localeid/)() | Alan'ın LCID'sini alır veya ayarlar. |
| [get_LockFields](./get_lockfields/)() override | Dahil edilen belgede alanların güncellenmesini önleyip önlemeyeceğini alır veya ayarlar. |
| [get_Result](../field/get_result/)() | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [get_Separator](../field/get_separator/)() | Alan ayırıcıyı temsil eden düğümü alır. **null** olabilir. |
| [get_SourceFullName](./get_sourcefullname/)() override | Belgenin konumunu alır veya ayarlar. |
| [get_Start](../field/get_start/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_TextConverter](./get_textconverter/)() override | Dahil edilen dosyanın formatı için metin dönüştürücünün adını alır veya ayarlar. |
| virtual [get_Type](../field/get_type/)() const | Microsoft Word alan türünü alır. |
| [GetFieldCode](../field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Alanı belgeden kaldırır. Alanın hemen sonrasındaki bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafını döndürür. Alan zaten kaldırılmışsa, **null** döndürür. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | [Aspose::Words::Fields::FieldInclude::get_BookmarkName](./get_bookmarkname/) için ayarlayıcı. |
| [set_IsDirty](../field/set_isdirty/)(bool) | [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) için ayarlayıcı. |
| [set_IsLocked](../field/set_islocked/)(bool) | [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) için ayarlayıcı. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) için ayarlayıcı. |
| [set_LockFields](./set_lockfields/)(bool) | [Aspose::Words::Fields::FieldInclude::get_LockFields](./get_lockfields/) için ayarlayıcı. |
| [set_Result](../field/set_result/)(const System::String\&) | [Aspose::Words::Fields::Field::get_Result](../field/get_result/) için ayarlayıcı. |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | [Aspose::Words::Fields::FieldInclude::get_SourceFullName](./get_sourcefullname/) için ayarlayıcı. |
| [set_TextConverter](./set_textconverter/)(const System::String\&) | [Aspose::Words::Fields::FieldInclude::get_TextConverter](./get_textconverter/) için ayarlayıcı. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Alan bağlantısını kaldırır. |
| [Update](../field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
| [Update](../field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |

## Örnekler



INCLUDE alanının nasıl oluşturulacağını ve özelliklerinin nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Yerel dosya sistemindeki başka bir belgenin bir bölümünü içe aktarmak için bir INCLUDE alanı kullanabiliriz.
// Bu alanla başvurduğumuz diğer belgedeki yer imi, bu içe aktarılan bölümü içerir.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldInclude>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInclude, true));
field->set_SourceFullName(get_MyDir() + u"Bookmarks.docx");
field->set_BookmarkName(u"MyBookmark1");
field->set_LockFields(false);
field->set_TextConverter(u"Microsoft Word");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->GetFieldCode(), u" INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"")->get_Success());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INCLUDE.docx");
```

## Ayrıca Bakınız

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
