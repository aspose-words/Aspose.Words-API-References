---
title: "طريقة Aspose::Words::Drawing::ShapeBase::get_HRef"
linktitle: "get_HRef"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::ShapeBase::get_HRef. يحصل على أو يعيّن عنوان الارتباط التشعبي الكامل لشكل في C++."
type: docs
weight: 24000
url: /ar/cpp/aspose.words.drawing/shapebase/get_href/
---
## ShapeBase::get_HRef method


الحصول أو تعيين عنوان الارتباط الكامل للشكل.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_HRef()
```

## ملاحظات


القيمة الافتراضية هي سلسلة فارغة.

فيما يلي أمثلة على القيم الصالحة لهذه الخاصية:

المسار الكامل: **https://www.aspose.com/**.

اسم الملف الكامل: **C:\\My Documents\\SalesReport.doc**.

المسار النسبي: **%../../../resource.txt**

اسم الملف النسبي: **%..\\My Documents\\SalesReport.doc**.

[Bookmark](../../../aspose.words/bookmark/) within another document: **https://www.aspose.com/Products/Default.aspx::Suites**

[Bookmark](../../../aspose.words/bookmark/) within this document: **%#BookmakName**.

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
