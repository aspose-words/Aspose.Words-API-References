---
title: "Aspose::Words::Drawing::Fill::SetImage method"
linktitle: "SetImage"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Fill::SetImage method. يغيّر نوع التعبئة إلى صورة واحدة في C++."
type: docs
weight: 42000
url: /ar/cpp/aspose.words.drawing/fill/setimage/
---
## Fill::SetImage(const System::ArrayPtr\<uint8_t\>\&) method


يغيّر نوع التعبئة إلى صورة واحدة.

```cpp
void Aspose::Words::Drawing::Fill::SetImage(const System::ArrayPtr<uint8_t> &imageBytes)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | مصفوفة بايتات الصورة. |

## أمثلة



يوضح كيفية تعيين نوع تعبئة الشكل كصورة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// هناك عدة طرق لتعيين الصورة.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// 1 -  استخدام اسم ملف محلي في النظام:
shape->get_Fill()->SetImage(get_ImageDir() + u"Logo.jpg");
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.FileName.docx");

// 2 -  تحميل ملف إلى مصفوفة بايت:
shape->get_Fill()->SetImage(System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg"));
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.ByteArray.docx");

// 3 -  من تدفق:
{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    shape->get_Fill()->SetImage(stream);
}
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.Stream.docx");
```

## انظر أيضًا

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## Fill::SetImage(const System::SharedPtr\<System::IO::Stream\>\&) method


يغيّر نوع التعبئة إلى صورة واحدة.

```cpp
void Aspose::Words::Drawing::Fill::SetImage(const System::SharedPtr<System::IO::Stream> &stream)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| تدفق | const System::SharedPtr\<System::IO::Stream\>\& | التدفق الذي يحتوي على بايتات الصورة. |

## أمثلة



يوضح كيفية تعيين نوع تعبئة الشكل كصورة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// هناك عدة طرق لتعيين الصورة.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// 1 -  استخدام اسم ملف محلي في النظام:
shape->get_Fill()->SetImage(get_ImageDir() + u"Logo.jpg");
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.FileName.docx");

// 2 -  تحميل ملف إلى مصفوفة بايت:
shape->get_Fill()->SetImage(System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg"));
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.ByteArray.docx");

// 3 -  من تدفق:
{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    shape->get_Fill()->SetImage(stream);
}
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.Stream.docx");
```

## انظر أيضًا

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## Fill::SetImage(const System::String\&) method


يغيّر نوع التعبئة إلى صورة واحدة.

```cpp
void Aspose::Words::Drawing::Fill::SetImage(const System::String &fileName)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fileName | const System::String\& | المسار إلى ملف الصورة. |

## أمثلة



يوضح كيفية تعيين نوع تعبئة الشكل كصورة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// هناك عدة طرق لتعيين الصورة.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// 1 -  استخدام اسم ملف محلي في النظام:
shape->get_Fill()->SetImage(get_ImageDir() + u"Logo.jpg");
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.FileName.docx");

// 2 -  تحميل ملف إلى مصفوفة بايت:
shape->get_Fill()->SetImage(System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg"));
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.ByteArray.docx");

// 3 -  من تدفق:
{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    shape->get_Fill()->SetImage(stream);
}
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.Stream.docx");
```

## انظر أيضًا

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
