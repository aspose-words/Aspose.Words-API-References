---
title: "Aspose::Words::PlainTextDocument فئة"
linktitle: "PlainTextDocument"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::PlainTextDocument فئة. يسمح باستخراج تمثيل النص العادي لمحتوى المستند. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 50000
url: /ar/cpp/aspose.words/plaintextdocument/
---
## PlainTextDocument class


يسمح باستخراج تمثيل نص عادي لمحتوى المستند. لمعرفة المزيد، زر مقالة الوثائق [Working with Text Document](https://docs.aspose.com/words/cpp/working-with-text-document/).

```cpp
class PlainTextDocument : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_BuiltInDocumentProperties](./get_builtindocumentproperties/)() const | يحصل على [BuiltInDocumentProperties](./get_builtindocumentproperties/) للمستند. |
| [get_CustomDocumentProperties](./get_customdocumentproperties/)() const | يحصل على [CustomDocumentProperties](./get_customdocumentproperties/) للمستند. |
| [get_Text](./get_text/)() const | يحصل على المحتوى النصي للمستند مدموجًا كسلسلة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PlainTextDocument](./plaintextdocument/)(const System::String\&) | ينشئ مستند نص عادي من ملف. يكتشف تنسيق الملف تلقائيًا. |
| [PlainTextDocument](./plaintextdocument/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | ينشئ مستند نص عادي من ملف. يسمح بتحديد خيارات إضافية مثل كلمة مرور التشفير. |
| [PlainTextDocument](./plaintextdocument/)(const System::SharedPtr\<System::IO::Stream\>\&) | ينشئ مستند نص عادي من تدفق. يكتشف تنسيق الملف تلقائيًا. |
| [PlainTextDocument](./plaintextdocument/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | ينشئ مستند نص عادي من تدفق. يسمح بتحديد خيارات إضافية مثل كلمة مرور التشفير. |
| [PlainTextDocument](./plaintextdocument/)(std::istream\&) |  |
| [PlainTextDocument](./plaintextdocument/)(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) |  |
| static [Type](./type/)() |  |

## أمثلة



يظهر كيفية تحميل محتويات مستند Microsoft Word كنص عادي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
