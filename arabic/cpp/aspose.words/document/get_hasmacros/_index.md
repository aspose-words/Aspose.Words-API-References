---
title: "Aspose::Words::Document::get_HasMacros طريقة"
linktitle: "get_HasMacros"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Document::get_HasMacros طريقة. تُرجع true إذا كان المستند يحتوي على مشروع VBA (ماكرو) في C++."
type: docs
weight: 30000
url: /ar/cpp/aspose.words/document/get_hasmacros/
---
## Document::get_HasMacros method


يعيد **true** إذا كان للمستند مشروع VBA (ماكرو).

```cpp
bool Aspose::Words::Document::get_HasMacros()
```


## أمثلة



يوضح كيفية استخدام حقول MACROBUTTON للسماح لنا بتشغيل ماكروات المستند بالنقر.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Macro.docm");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_TRUE(doc->get_HasMacros());

// أدرج حقل MACROBUTTON، واشر إلى أحد ماكروات المستند بالاسم في خاصية MacroName.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldMacroButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldMacroButton, true));
field->set_MacroName(u"MyMacro");
field->set_DisplayText(System::String(u"Double click to run macro: ") + field->get_MacroName());

ASSERT_EQ(u" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field->GetFieldCode());

// استخدم الخاصية للإشارة إلى "ViewZoom200"، ماكرو يأتي مع Microsoft Word.
// يمكننا العثور على جميع الماكرو الأخرى عبر View -> Macros (القائمة المنسدلة) -> View Macros.
// في ذلك القائمة، اختر "Word Commands" من القائمة المنسدلة "Macros in:".
// إذا كان المستند يحتوي على ماكرو مخصص يحمل نفس اسم ماكرو أساسي،
// سيكون ماكرو الخاص بنا هو الذي يتم تشغيله بواسطة حقل MACROBUTTON.
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldMacroButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldMacroButton, true));
field->set_MacroName(u"ViewZoom200");
field->set_DisplayText(System::String(u"Run ") + field->get_MacroName());

ASSERT_EQ(u" MACROBUTTON  ViewZoom200 Run ViewZoom200", field->GetFieldCode());

// احفظ المستند كنوع مستند يدعم الماكرو.
doc->Save(get_ArtifactsDir() + u"Field.MACROBUTTON.docm");
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
