---
title: "Aspose::Words::DocumentBuilder::InsertShape method"
linktitle: "InsertShape"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBuilder::InsertShape. تُدرج شكلًا عائمًا مع موقع وحجم ونوع لف النص المحددين في C++."
type: docs
weight: 45000
url: /ar/cpp/aspose.words/documentbuilder/insertshape/
---
## DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


يقوم بإدراج شكل عائم بحرية بالموقع والحجم ونوع التفاف النص المحددين.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType shapeType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| shapeType | Aspose::Words::Drawing::ShapeType | نوع الشكل المراد إدراجه في المستند |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | يحدد من أين يُقاس البعد الأفقي إلى الشكل. |
| left | double | المسافة بالنقاط من الأصل إلى الجانب الأيسر من الشكل. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | يحدد من أين يتم قياس المسافة العمودية إلى الشكل. |
| top | double | المسافة بالنقاط من الأصل إلى الجانب العلوي للشكل. |
| العرض | double | عرض الشكل بالنقاط. |
| الارتفاع | double | ارتفاع الشكل بالنقاط. |
| wrapType | Aspose::Words::Drawing::WrapType | يحدد كيفية لف النص حول الشكل. |

### ReturnValue

عقدة الشكل التي تم إدراجها.

## أمثلة



يوضح كيفية إدراج أشكال DML في مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// فيما يلي نوعان من التغليف التي قد تمتلكها الأشكال.
// 1 -  عائم:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::TopCornersRounded, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 100, 50, 50, Aspose::Words::Drawing::WrapType::None);

// 2 -  مدمج:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::DiagonalCornersRounded, 50, 50);

// إذا كنت بحاجة لإنشاء أشكال "غير أولية"، مثل SingleCornerSnipped، TopCornersSnipped، DiagonalCornersSnipped،
// TopCornersOneRoundedOneSnipped، SingleCornerRounded، TopCornersRounded، أو DiagonalCornersRounded،
// ثم احفظ المستند مع امتثال "Strict" أو "Transitional"، مما يسمح بحفظ الشكل كـ DML.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeInsertion.docx", saveOptions);
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType, double, double) method


يقوم بإدراج شكل داخل السطر بالنوع والحجم المحددين.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType shapeType, double width, double height)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| shapeType | Aspose::Words::Drawing::ShapeType | نوع الشكل الذي سيتم إدراجه في المستند. |
| العرض | double | عرض الشكل بالنقاط. |
| الارتفاع | double | ارتفاع الشكل بالنقاط. |

### ReturnValue

عقدة الشكل التي تم إدراجها.

## أمثلة



يوضح كيفية إدراج أشكال DML في مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// فيما يلي نوعان من التغليف التي قد تمتلكها الأشكال.
// 1 -  عائم:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::TopCornersRounded, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 100, 50, 50, Aspose::Words::Drawing::WrapType::None);

// 2 -  مدمج:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::DiagonalCornersRounded, 50, 50);

// إذا كنت بحاجة لإنشاء أشكال "غير أولية"، مثل SingleCornerSnipped، TopCornersSnipped، DiagonalCornersSnipped،
// TopCornersOneRoundedOneSnipped، SingleCornerRounded، TopCornersRounded، أو DiagonalCornersRounded،
// ثم احفظ المستند مع امتثال "Strict" أو "Transitional"، مما يسمح بحفظ الشكل كـ DML.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeInsertion.docx", saveOptions);
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
