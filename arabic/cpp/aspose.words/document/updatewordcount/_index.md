---
title: "طريقة Aspose::Words::Document::UpdateWordCount"
linktitle: "UpdateWordCount"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::UpdateWordCount. يُحدّث خصائص عدد الكلمات في المستند في C++."
type: docs
weight: 101000
url: /ar/cpp/aspose.words/document/updatewordcount/
---
## Document::UpdateWordCount() method


يحدّث خصائص عدد الكلمات في المستند.

```cpp
void Aspose::Words::Document::UpdateWordCount()
```

## ملاحظات


[UpdateWordCount](./) recalculates and updates Characters, [Words](../../) and Paragraphs properties in the [BuiltInDocumentProperties](../get_builtindocumentproperties/) collection of the [Document](../).

لاحظ أن [UpdateWordCount](./) لا يُحدّث خصائص عدد الأسطر والصفحات. استخدم التحميل الزائد لـ [UpdateWordCount](./) ومرّر القيمة **true** كمعامل للقيام بذلك.

عند استخدام نسخة تقييمية، سيتم تضمين علامة التقييم المائية أيضًا في عدد الكلمات.

## أمثلة



يوضح كيفية تحديث جميع تسميات القوائم في مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(System::String(u"Ut enim ad minim veniam, ") + u"quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// لا يتتبع Aspose.Words مقاييس المستند مثل هذه في الوقت الفعلي.
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Paragraphs());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

// للحصول على قيم دقيقة لثلاثة من هذه الخصائص، سنحتاج إلى تحديثها يدويًا.
doc->UpdateWordCount();

ASSERT_EQ(196, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(36, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Paragraphs());

// لعدد الأسطر، سنحتاج إلى استدعاء تحميل زائد محدد لطريقة التحديث.
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

doc->UpdateWordCount(true);

ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Lines());
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::UpdateWordCount(bool) method


يُحدّث خصائص عدد الكلمات في المستند، ويُحدّث اختياريًا خاصية [Lines](../../../aspose.words.properties/builtindocumentproperties/get_lines/).

```cpp
void Aspose::Words::Document::UpdateWordCount(bool updateLinesCount)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| updateLinesCount | bool | **true** إذا كان يجب حساب عدد الأسطر في المستند. |

## أمثلة



يوضح كيفية تحديث جميع تسميات القوائم في مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(System::String(u"Ut enim ad minim veniam, ") + u"quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// لا يتتبع Aspose.Words مقاييس المستند مثل هذه في الوقت الفعلي.
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Paragraphs());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

// للحصول على قيم دقيقة لثلاثة من هذه الخصائص، سنحتاج إلى تحديثها يدويًا.
doc->UpdateWordCount();

ASSERT_EQ(196, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(36, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Paragraphs());

// لعدد الأسطر، سنحتاج إلى استدعاء تحميل زائد محدد لطريقة التحديث.
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

doc->UpdateWordCount(true);

ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Lines());
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
