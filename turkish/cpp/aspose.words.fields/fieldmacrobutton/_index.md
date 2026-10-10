---
title: "Aspose::Words::Fields::FieldMacroButton sınıfı"
linktitle: "FieldMacroButton"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldMacroButton sınıfı. MACROBUTTON alanını uygular. Daha fazla bilgi edinmek için C++'deki belge makalesini ziyaret edin."
type: docs
weight: 65000
url: /tr/cpp/aspose.words.fields/fieldmacrobutton/
---
## FieldMacroButton class


MACROBUTTON alanını uygular. Daha fazla bilgi edinmek için [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldMacroButton : public Aspose::Words::Fields::Field,
                         public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Görüntülenen alan sonucunu temsil eden metni alır. |
| [get_DisplayText](./get_displaytext/)() | Makroyu veya komutu çalıştırmak için seçilen "düğme" olarak görünecek metni alır veya ayarlar. |
| [get_End](./get_end/)() override | Alan sonunu temsil eden düğümü alır. |
| [get_End](../field/get_end/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldEnd](../field/get_fieldend/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldStart](../field/get_fieldstart/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_Format](../field/get_format/)() | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../fieldformat/) nesnesi alır. |
| [get_IsDirty](../field/get_isdirty/)() | Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [get_IsLocked](../field/get_islocked/)() | Alan'ın kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır veya ayarlar. |
| [get_LocaleId](../field/get_localeid/)() | Alan'ın LCID'sini alır veya ayarlar. |
| [get_MacroName](./get_macroname/)() | Çalıştırılacak makro veya komutun adını alır veya ayarlar. |
| [get_Result](../field/get_result/)() | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [get_Separator](./get_separator/)() override | Alan ayırıcıyı temsil eden düğümü alır. **null** olabilir. |
| [get_Start](./get_start/)() override | Alan başlangıcını temsil eden düğümü alır. |
| [get_Start](../field/get_start/)() const | Alan başlangıcını temsil eden düğümü alır. |
| virtual [get_Type](../field/get_type/)() const | Microsoft Word alan türünü alır. |
| [GetFieldCode](../field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Alanı belgeden kaldırır. Alanın hemen sonrasındaki bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafını döndürür. Alan zaten kaldırılmışsa, **null** döndürür. |
| [set_DisplayText](./set_displaytext/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldMacroButton::get_DisplayText](./get_displaytext/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) için ayarlayıcı. |
| [set_IsLocked](../field/set_islocked/)(bool) | [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) için ayarlayıcı. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) için ayarlayıcı. |
| [set_MacroName](./set_macroname/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldMacroButton::get_MacroName](./get_macroname/). |
| [set_Result](../field/set_result/)(const System::String\&) | [Aspose::Words::Fields::Field::get_Result](../field/get_result/) için ayarlayıcı. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Alan bağlantısını kaldırır. |
| [Update](../field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
| [Update](../field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
## Açıklamalar


Bir makro veya komutun çalıştırılmasına izin verir.

Aspose.Words içinde bu alan bir birleştirme alanı olarak da işlev görebilir.

## Örnekler



MACROBUTTON alanlarını kullanarak bir belgenin makrolarını tıklayarak çalıştırmamızı nasıl sağlayacağımızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Macro.docm");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_TRUE(doc->get_HasMacros());

// Bir MACROBUTTON alanı ekleyin ve MacroName özelliğinde belgenin makrolarından birine adını referans verin.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldMacroButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldMacroButton, true));
field->set_MacroName(u"MyMacro");
field->set_DisplayText(System::String(u"Double click to run macro: ") + field->get_MacroName());

ASSERT_EQ(u" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field->GetFieldCode());

// Microsoft Word ile gelen bir makro olan "ViewZoom200"'e başvurmak için özelliği kullanın.
// Tüm diğer makroları Görünüm -> Makrolar (açılır menü) -> Makroları Görün üzerinden bulabiliriz.
// Bu menüde, "Macros in:" açılır menüsünden "Word Commands" seçeneğini seçin.
// Belgeniz aynı ada sahip yerleşik bir makro ile aynı ada sahip bir özel makro içeriyorsa,
// özel makronuz, MACROBUTTON alanının çalıştırdığı makro olacaktır.
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldMacroButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldMacroButton, true));
field->set_MacroName(u"ViewZoom200");
field->set_DisplayText(System::String(u"Run ") + field->get_MacroName());

ASSERT_EQ(u" MACROBUTTON  ViewZoom200 Run ViewZoom200", field->GetFieldCode());

// Belgeyi makro etkin bir belge türü olarak kaydedin.
doc->Save(get_ArtifactsDir() + u"Field.MACROBUTTON.docm");
```

## Ayrıca Bakınız

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
