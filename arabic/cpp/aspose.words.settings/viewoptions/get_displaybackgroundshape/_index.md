---
title: "Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape method"
linktitle: "get_DisplayBackgroundShape"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape method. يتحكم في عرض الشكل الخلفي في عرض تخطيط الطباعة في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.settings/viewoptions/get_displaybackgroundshape/
---
## ViewOptions::get_DisplayBackgroundShape method


يتحكم في عرض الشكل الخلفي في عرض تخطيط الطباعة.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape() const
```


## أمثلة



يظهر كيفية إخفاء/عرض صور خلفية المستند في خيارات العرض.
```cpp
// استخدم سلسلة HTML لإنشاء مستند جديد بلون خلفية ثابت.
const System::String html = u"<html>\r\n                <body style='background-color: blue'>\r\n                    <p>Hello world!</p>\r\n                </body>\r\n            </html>";

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_Unicode()->GetBytes(html)));

// المصدر للمستند يحتوي على خلفية بلون ثابت،
// وجوده سيضبط علم "DisplayBackgroundShape" إلى "true".
ASSERT_TRUE(doc->get_ViewOptions()->get_DisplayBackgroundShape());

// احتفظ بـ "DisplayBackgroundShape" كـ "true" لجعل المستند يعرض لون الخلفية.
// قد يؤثر ذلك على بعض ألوان النص لتحسين الرؤية.
// اضبط "DisplayBackgroundShape" إلى "false" لعدم عرض لون الخلفية.
doc->get_ViewOptions()->set_DisplayBackgroundShape(displayBackgroundShape);

doc->Save(get_ArtifactsDir() + u"ViewOptions.DisplayBackgroundShape.docx");
```

## انظر أيضًا

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
