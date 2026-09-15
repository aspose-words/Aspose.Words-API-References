---
title: "Aspose::Words::ControlChar::Cr طريقة"
linktitle: "Cr"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ControlChar::Cr طريقة. حرف عودة السطر: \"\\x000d\" أو \"\\r\". نفس ParagraphBreak في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/controlchar/cr/
---
## ControlChar::Cr method


حرف عودة السطر: "\x000d" أو "\r". نفس [ParagraphBreak](../paragraphbreak/).

```cpp
static System::String & Aspose::Words::ControlChar::Cr()
```


## أمثلة



يعرض كيفية استخدام الأحرف التحكمية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إدراج فقرات بنص باستخدام DocumentBuilder.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// تحويل المستند إلى صيغة نصية يكشف أن الأحرف التحكمية
// تمثل بعض العناصر الهيكلية للمستند، مثل فواصل الصفحات.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + System::String::Format(u"Hello again!{0}", Aspose::Words::ControlChar::Cr()) + Aspose::Words::ControlChar::PageBreak(), doc->GetText());

// عند تحويل مستند إلى صيغة سلسلة،
// يمكننا حذف بعض الأحرف التحكمية باستخدام طريقة Trim.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + u"Hello again!", doc->GetText().Trim());
```

## انظر أيضًا

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
