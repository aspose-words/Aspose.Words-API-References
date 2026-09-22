---
title: "Aspose::Words::Font::get_TextEffect طريقة"
linktitle: "get_TextEffect"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Font::get_TextEffect طريقة. يحصل على أو يحدد تأثير الرسوم المتحركة للخط في C++."
type: docs
weight: 47000
url: /ar/cpp/aspose.words/font/get_texteffect/
---
## Font::get_TextEffect method


الحصول أو تعيين تأثير حركة الخط.

```cpp
Aspose::Words::TextEffect Aspose::Words::Font::get_TextEffect()
```


## أمثلة



يظهر كيفية تطبيق تأثير بصري على run.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_TextEffect(Aspose::Words::TextEffect::SparkleText);

builder->Writeln(u"Text with a sparkle effect.");

// الإصدارات القديمة من Microsoft Word تدعم فقط تأثيرات الرسوم المتحركة للخط.
doc->Save(get_ArtifactsDir() + u"Font.SparklingText.doc");
```

## انظر أيضًا

* Enum [TextEffect](../../texteffect/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
