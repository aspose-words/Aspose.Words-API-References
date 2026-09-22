---
title: "Aspose::Words::Fields::FieldGoToButton sınıfı"
linktitle: "FieldGoToButton"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldGoToButton sınıfı. GOTOBUTTON alanını uygular. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 51000
url: /tr/cpp/aspose.words.fields/fieldgotobutton/
---
## FieldGoToButton class


GOTOBUTTON alanını uygular. Daha fazla bilgi edinmek için, [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldGoToButton : public Aspose::Words::Fields::Field
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Görüntülenen alan sonucunu temsil eden metni alır. |
| [get_DisplayText](./get_displaytext/)() | Belgede görünen \"button\" metnini alır veya ayarlar, böylece atlamayı etkinleştirmek için seçilebilir. |
| [get_End](../field/get_end/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldEnd](../field/get_fieldend/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldStart](../field/get_fieldstart/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_Format](../field/get_format/)() | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../fieldformat/) nesnesi alır. |
| [get_IsDirty](../field/get_isdirty/)() | Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [get_IsLocked](../field/get_islocked/)() | Alan'ın kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır veya ayarlar. |
| [get_LocaleId](../field/get_localeid/)() | Alan'ın LCID'sini alır veya ayarlar. |
| [get_Location](./get_location/)() | Atlanacak bir yer imi, sayfa numarası veya başka bir öğenin adını alır veya ayarlar. |
| [get_Result](../field/get_result/)() | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [get_Separator](../field/get_separator/)() | Alan ayırıcıyı temsil eden düğümü alır. **null** olabilir. |
| [get_Start](../field/get_start/)() const | Alan başlangıcını temsil eden düğümü alır. |
| virtual [get_Type](../field/get_type/)() const | Microsoft Word alan türünü alır. |
| [GetFieldCode](../field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Alanı belgeden kaldırır. Alanın hemen sonrasındaki bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafını döndürür. Alan zaten kaldırılmışsa, **null** döndürür. |
| [set_DisplayText](./set_displaytext/)(const System::String\&) | [Aspose::Words::Fields::FieldGoToButton::get_DisplayText](./get_displaytext/) için ayarlayıcı. |
| [set_IsDirty](../field/set_isdirty/)(bool) | [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) için ayarlayıcı. |
| [set_IsLocked](../field/set_islocked/)(bool) | [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) için ayarlayıcı. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) için ayarlayıcı. |
| [set_Location](./set_location/)(const System::String\&) | [Aspose::Words::Fields::FieldGoToButton::get_Location](./get_location/) için ayarlayıcı. |
| [set_Result](../field/set_result/)(const System::String\&) | [Aspose::Words::Fields::Field::get_Result](../field/get_result/) için ayarlayıcı. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Alan bağlantısını kaldırır. |
| [Update](../field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
| [Update](../field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |

## Örnekler



GOTOBUTTON alanının nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir GOTOBUTTON alanı ekleyin. Microsoft Word'de bu alana çift tıkladığımızda,
// İmleç, Location özelliğinin başvurduğu yer iminin adına götürülür.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldGoToButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldGoToButton, true));
field->set_DisplayText(u"My Button");
field->set_Location(u"MyBookmark");

ASSERT_EQ(u" GOTOBUTTON  MyBookmark My Button", field->GetFieldCode());

// Alan tarafından başvurulacak geçerli bir yer imi ekleyin.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(field->get_Location());
builder->Writeln(u"Bookmark text contents.");
builder->EndBookmark(field->get_Location());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.GOTOBUTTON.docx");
```

## Ayrıca Bakınız

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
