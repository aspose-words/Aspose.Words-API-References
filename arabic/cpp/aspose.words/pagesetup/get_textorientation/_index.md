---
title: "طريقة Aspose::Words::PageSetup::get_TextOrientation"
linktitle: "get_TextOrientation"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::PageSetup::get_TextOrientation. يسمح بتحديد TextOrientation للصفحة بأكملها. القيمة الافتراضية هي Horizontal في C++."
type: docs
weight: 45000
url: /ar/cpp/aspose.words/pagesetup/get_textorientation/
---
## PageSetup::get_TextOrientation method


يسمح بتحديد [TextOrientation](./) للصفحة بأكملها. القيمة الافتراضية هي [Horizontal](../../textorientation/)

```cpp
Aspose::Words::TextOrientation Aspose::Words::PageSetup::get_TextOrientation()
```


## أمثلة



يوضح كيفية تعيين اتجاه النص.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// قم بتعيين الخاصية \"TextOrientation\" إلى \"TextOrientation.Upward\" لتدوير جميع النص 90 درجة
// إلى اليمين بحيث يصبح كل النص من اليسار إلى اليمين الآن من أعلى إلى أسفل.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_TextOrientation(Aspose::Words::TextOrientation::Upward);

doc->Save(get_ArtifactsDir() + u"PageSetup.SetTextOrientation.docx");
```

## انظر أيضًا

* Enum [TextOrientation](../../textorientation/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
