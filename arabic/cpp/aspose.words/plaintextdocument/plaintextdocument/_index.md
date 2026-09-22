---
title: "منشئ Aspose::Words::PlainTextDocument::PlainTextDocument"
linktitle: "PlainTextDocument"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "منشئ Aspose::Words::PlainTextDocument::PlainTextDocument. ينشئ مستند نص عادي من تدفق. يكتشف تنسيق الملف تلقائيًا في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/plaintextdocument/plaintextdocument/
---
## PlainTextDocument::PlainTextDocument(const System::SharedPtr\<System::IO::Stream\>\&) constructor


ينشئ مستند نص عادي من تدفق. يكتشف تنسيق الملف تلقائيًا.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::SharedPtr<System::IO::Stream> &stream)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| تدفق | const System::SharedPtr\<System::IO::Stream\>\& | التدفق الذي يتم استخراج النص منه. |
## ملاحظات


يجب أن يكون المستند مخزنًا في بداية الـStream. يجب أن يدعم الـStream وضعية عشوائية.

## أمثلة



يوضح كيفية تحميل محتويات مستند Microsoft Word كنص عادي باستخدام التدفق.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
doc->Save(get_ArtifactsDir() + u"PlainTextDocument.LoadFromStream.docx");

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"PlainTextDocument.LoadFromStream.docx", System::IO::FileMode::Open);
    auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(stream);

    ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
}
```

## انظر أيضًا

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


ينشئ مستند نص عادي من تدفق. يسمح بتحديد خيارات إضافية مثل كلمة مرور التشفير.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::SharedPtr<System::IO::Stream> &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| تدفق | const System::SharedPtr\<System::IO::Stream\>\& | التدفق الذي يتم استخراج النص منه. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | خيارات إضافية لاستخدامها عند تحميل مستند. يمكن أن تكون **null**. |
## ملاحظات


يجب أن يكون المستند مخزنًا في بداية الـStream. يجب أن يدعم الـStream وضعية عشوائية.

## أمثلة



يوضح كيفية تحميل محتويات مستند Microsoft Word مشفر كنص عادي باستخدام التدفق.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.LoadFromStreamWithOptions.docx", saveOptions);

auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_Password(u"MyPassword");

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"PlainTextDocument.LoadFromStreamWithOptions.docx", System::IO::FileMode::Open);
    auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(stream, loadOptions);

    ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
}
```

## انظر أيضًا

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(const System::String\&) constructor


ينشئ مستند نص عادي من ملف. يكتشف تنسيق الملف تلقائيًا.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::String &fileName)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fileName | const System::String\& | اسم الملف لاستخراج النص منه. |

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

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


ينشئ مستند نص عادي من ملف. يسمح بتحديد خيارات إضافية مثل كلمة مرور التشفير.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::String &fileName, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fileName | const System::String\& | اسم الملف لاستخراج النص منه. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | خيارات إضافية لاستخدامها عند تحميل مستند. يمكن أن تكون **null**. |

## أمثلة



يوضح كيفية تحميل محتويات مستند Microsoft Word مشفر كنص عادي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.LoadEncrypted.docx", saveOptions);

auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_Password(u"MyPassword");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.LoadEncrypted.docx", loadOptions);

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
```

## انظر أيضًا

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(std::istream\&) constructor




```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(std::istream &stream)
```

## انظر أيضًا

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor




```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(std::istream &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```

## انظر أيضًا

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
