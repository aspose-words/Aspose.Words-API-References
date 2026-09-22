---
title: "Aspose::Words::TextEffect enum"
linktitle: "TextEffect"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::TextEffect enum. تأثير الرسوم المتحركة لتشغيل النصوص في C++."
type: docs
weight: 123000
url: /ar/cpp/aspose.words/texteffect/
---
## TextEffect enum


تأثير الرسوم المتحركة لتشغيلات النص.

```cpp
enum class TextEffect
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 0 |  |
| LasVegasLights | 1 |  |
| BlinkingBackground | 2 |  |
| SparkleText | 3 |  |
| MarchingBlackAnts | 4 |  |
| MarchingRedAnts | 5 |  |
| Shimmer | 6 |  |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
