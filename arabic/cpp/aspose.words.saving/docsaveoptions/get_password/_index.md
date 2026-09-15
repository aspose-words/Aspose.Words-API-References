---
title: "طريقة Aspose::Words::Saving::DocSaveOptions::get_Password"
linktitle: "get_Password"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::DocSaveOptions::get_Password. يحصل على/يضبط كلمة مرور لتشفير المستند باستخدام طريقة تشفير RC4 في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.saving/docsaveoptions/get_password/
---
## DocSaveOptions::get_Password method


يحصل/يضبط كلمة مرور لتشفير المستند باستخدام طريقة تشفير RC4.

```cpp
System::String Aspose::Words::Saving::DocSaveOptions::get_Password() const
```

## ملاحظات


لحفظ المستند بدون تشفير يجب أن تكون هذه الخاصية **null** أو سلسلة فارغة.

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
