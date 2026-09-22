---
title: "Aspose::Words::Fields::FieldSymbol::get_FontName طريقة"
linktitle: "get_FontName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldSymbol::get_FontName طريقة. يحصل أو يضبط اسم الخط الخاص بالحرف المستخرج بواسطة الحقل في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.fields/fieldsymbol/get_fontname/
---
## FieldSymbol::get_FontName method


يحصل أو يضبط اسم الخط الخاص بالحرف المستخرج بواسطة الحقل.

```cpp
System::String Aspose::Words::Fields::FieldSymbol::get_FontName()
```


## أمثلة



يعرض كيفية استخدام حقل SYMBOL.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// فيما يلي ثلاث طرق لاستخدام حقل SYMBOL لعرض حرف واحد.
// 1 -  أضف حقل SYMBOL يعرض رمز © (حقوق النشر)، المحدد برمز حرف ANSI:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));

// رمز حرف ANSI "U+00A9" أو "169" في الشكل العددي مخصص لرمز حقوق النشر.
field->set_CharacterCode(System::Convert::ToString(0x00a9));
field->set_IsAnsi(true);

ASSERT_EQ(u" SYMBOL  169 \\a", field->GetFieldCode());

builder->Writeln(u" Line 1");

// 2 -  أضف حقل SYMBOL يعرض رمز ∞ (اللانهاية)، وعدّل مظهره:
field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));

// في Unicode، يشغل رمز اللانهاية الرمز "221E".
field->set_CharacterCode(System::Convert::ToString(0x221E));
field->set_IsUnicode(true);

// غيّر خط رمزنا بعد استخدام خريطة الأحرف في Windows
// للتأكد من أن الخط يمكنه تمثيل ذلك الرمز.
field->set_FontName(u"Calibri");
field->set_FontSize(u"24");

// يمكننا تعيين هذه العلامة للرموز الطويلة لجعلها لا تدفع بقية النص أسفل سطرها.
field->set_DontAffectsLineSpacing(true);

ASSERT_EQ(u" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field->GetFieldCode());

builder->Writeln(u"Line 2");

// 3 - أضف حقل SYMBOL يعرض الحرف あ،
// مع خط يدعم مجموعة الترميز Shift-JIS (Windows-932):
field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));
field->set_FontName(u"MS Gothic");
field->set_CharacterCode(System::Convert::ToString(0x82A0));
field->set_IsShiftJis(true);

ASSERT_EQ(u" SYMBOL  33440 \\f \"MS Gothic\" \\j", field->GetFieldCode());

builder->Write(u"Line 3");

doc->Save(get_ArtifactsDir() + u"Field.SYMBOL.docx");
```

## انظر أيضًا

* Class [FieldSymbol](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
