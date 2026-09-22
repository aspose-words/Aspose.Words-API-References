---
title: "Aspose::Words::Document::get_HasMacros metodu"
linktitle: "get_HasMacros"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_HasMacros metodu. Belgenin C++'ta bir VBA projesi (makrolar) içeriyorsa true döndürür."
type: docs
weight: 30000
url: /tr/cpp/aspose.words/document/get_hasmacros/
---
## Document::get_HasMacros method


Belgenin bir VBA projesi (makrolar) varsa **true** döndürür.

```cpp
bool Aspose::Words::Document::get_HasMacros()
```


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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
