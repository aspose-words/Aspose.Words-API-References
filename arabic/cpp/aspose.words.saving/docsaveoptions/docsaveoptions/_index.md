---
title: "Aspose::Words::Saving::DocSaveOptions::DocSaveOptions constructor"
linktitle: "DocSaveOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::DocSaveOptions::DocSaveOptions constructor. يهيئ مثيلاً جديداً من هذه الفئة يمكن استخدامه لحفظ مستند بتنسيق Doc في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.saving/docsaveoptions/docsaveoptions/
---
## DocSaveOptions::DocSaveOptions() constructor


يهيئ مثيلاً جديداً من هذه الفئة يمكن استخدامه لحفظ مستند بتنسيق [Doc](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::DocSaveOptions::DocSaveOptions()
```


## أمثلة



يوضح كيفية تعيين خيارات الحفظ لتنسيقات Microsoft Word القديمة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto options = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>(Aspose::Words::SaveFormat::Doc);

// حدد كلمة مرور ستحمي تحميل المستند بواسطة Microsoft Word أو Aspose.Words.
// لاحظ أن هذا لا يقوم بتشفير محتويات المستند بأي شكل.
options->set_Password(u"MyPassword");

// إذا كان المستند يحتوي على قسيمة توجيه، يمكننا الحفاظ عليها أثناء الحفظ بتعيين هذه العلامة إلى true.
options->set_SaveRoutingSlip(true);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc", options);

// لكي نتمكن من تحميل المستند،
// سنحتاج إلى تطبيق كلمة المرور التي حددناها في كائن DocSaveOptions داخل كائن LoadOptions.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc");
})(), Aspose::Words::IncorrectPasswordException);

auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"MyPassword");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc", loadOptions);

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## انظر أيضًا

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## DocSaveOptions::DocSaveOptions(Aspose::Words::SaveFormat) constructor


يهيئ مثيلاً جديداً من هذه الفئة يمكن استخدامه لحفظ مستند بتنسيق [Doc](../../../aspose.words/saveformat/) أو [Dot](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::DocSaveOptions::DocSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | يمكن أن يكون [Doc](../../../aspose.words/saveformat/) أو [Dot](../../../aspose.words/saveformat/). |

## أمثلة



يوضح كيفية تعيين خيارات الحفظ لتنسيقات Microsoft Word القديمة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto options = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>(Aspose::Words::SaveFormat::Doc);

// حدد كلمة مرور ستحمي تحميل المستند بواسطة Microsoft Word أو Aspose.Words.
// لاحظ أن هذا لا يقوم بتشفير محتويات المستند بأي شكل.
options->set_Password(u"MyPassword");

// إذا كان المستند يحتوي على قسيمة توجيه، يمكننا الحفاظ عليها أثناء الحفظ بتعيين هذه العلامة إلى true.
options->set_SaveRoutingSlip(true);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc", options);

// لكي نتمكن من تحميل المستند،
// سنحتاج إلى تطبيق كلمة المرور التي حددناها في كائن DocSaveOptions داخل كائن LoadOptions.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc");
})(), Aspose::Words::IncorrectPasswordException);

auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"MyPassword");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc", loadOptions);

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
