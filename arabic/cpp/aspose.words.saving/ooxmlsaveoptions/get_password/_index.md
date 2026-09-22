---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_Password طريقة"
linktitle: "get_Password"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_Password طريقة. يحصل/يضبط كلمة مرور لتشفير المستند باستخدام خوارزمية تشفير ECMA376 القياسية في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.saving/ooxmlsaveoptions/get_password/
---
## OoxmlSaveOptions::get_Password method


يحصل/يعيّن كلمة مرور لتشفير المستند باستخدام خوارزمية تشفير ECMA376 Standard.

```cpp
System::String Aspose::Words::Saving::OoxmlSaveOptions::get_Password() const
```

## ملاحظات


لحفظ المستند بدون تشفير يجب أن تكون هذه الخاصية **null** أو سلسلة فارغة.

## أمثلة



يعرض كيفية إنشاء مستند Office Open XML مشفر بكلمة مرور.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx", saveOptions);

// لن نتمكن من فتح هذا المستند باستخدام Microsoft Word أو
// Aspose.Words دون توفير كلمة المرور الصحيحة.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx");
})(), Aspose::Words::IncorrectPasswordException);

// افتح المستند المشفر بتمرير كلمة المرور الصحيحة في كائن LoadOptions.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"MyPassword"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## انظر أيضًا

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
