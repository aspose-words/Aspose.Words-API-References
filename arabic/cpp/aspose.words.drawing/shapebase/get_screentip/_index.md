---
title: "طريقة Aspose::Words::Drawing::ShapeBase::get_ScreenTip"
linktitle: "get_ScreenTip"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::ShapeBase::get_ScreenTip. يحدد النص المعروض عندما يتحرك مؤشر الفأرة فوق الشكل في C++."
type: docs
weight: 46000
url: /ar/cpp/aspose.words.drawing/shapebase/get_screentip/
---
## ShapeBase::get_ScreenTip method


يحدد النص المعروض عندما يتحرك مؤشر الفأرة فوق الشكل.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_ScreenTip()
```

## ملاحظات


القيمة الافتراضية هي سلسلة فارغة.

## أمثلة



يوضح كيفية إدراج شكل يحتوي على صورة، وهو أيضًا ارتباط تشعبي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_HRef(u"https://forum.aspose.com/");
shape->set_Target(u"New Window");
shape->set_ScreenTip(u"Aspose.Words Support Forums");

// الضغط على Ctrl + النقر بالزر الأيسر على الشكل في Microsoft Word سيفتح نافذة متصفح ويب جديدة
// ويأخذنا إلى الارتباط التشعبي في خاصية "HRef".
doc->Save(get_ArtifactsDir() + u"Image.InsertImageWithHyperlink.docx");
```

## انظر أيضًا

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
