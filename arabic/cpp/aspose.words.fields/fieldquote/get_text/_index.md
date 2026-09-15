---
title: "طريقة Aspose::Words::Fields::FieldQuote::get_Text"
linktitle: "get_Text"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldQuote::get_Text. يحصل على النص أو يضبطه للاسترجاع في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fieldquote/get_text/
---
## FieldQuote::get_Text method


يحصل أو يضبط النص المراد استرجاعه.

```cpp
System::String Aspose::Words::Fields::FieldQuote::get_Text()
```


## أمثلة



يُظهر كيفية استخدام حقل QUOTE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج حقل QUOTE، الذي سيعرض قيمة خاصية Text الخاصة به.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
field->set_Text(u"\"Quoted text\"");

ASSERT_EQ(u" QUOTE  \"\\\"Quoted text\\\"\"", field->GetFieldCode());

// أدرج حقل QUOTE وضمّن داخله حقل DATE.
// تُحدّث حقول DATE قيمتها إلى التاريخ الحالي في كل مرة نفتح فيها المستند باستخدام Microsoft Word.
// إدراج حقل DATE داخل حقل QUOTE بهذه الطريقة سيجمد قيمته
// إلى التاريخ الذي أنشأنا فيه المستند.
builder->Write(u"\nDocument creation date: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
builder->MoveTo(field->get_Separator());
builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true);

ASSERT_EQ(System::String(u" QUOTE \u0013 DATE \u0014") + System::DateTime::get_Now().get_Date().ToShortDateString() + u"\u0015", field->GetFieldCode());

// حدّث جميع الحقول لعرض نتائجها الصحيحة.
doc->UpdateFields();

ASSERT_EQ(u"\"Quoted text\"", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.QUOTE.docx");
```

## انظر أيضًا

* Class [FieldQuote](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
