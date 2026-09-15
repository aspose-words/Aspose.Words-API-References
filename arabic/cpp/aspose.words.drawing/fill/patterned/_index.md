---
title: "طريقة Aspose::Words::Drawing::Fill::Patterned"
linktitle: "منقوش"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Fill::Patterned. تُعيّن التعبئة المحددة إلى نمط في C++."
type: docs
weight: 26000
url: /ar/cpp/aspose.words.drawing/fill/patterned/
---
## Fill::Patterned(Aspose::Words::Drawing::PatternType) method


يضبط التعبئة المحددة لتصبح نمطًا.

```cpp
void Aspose::Words::Drawing::Fill::Patterned(Aspose::Words::Drawing::PatternType patternType)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| patternType | Aspose::Words::Drawing::PatternType | [PatternType](../../patterntype/) |

## أمثلة



يوضح كيفية تعيين نمط لشكل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();

std::cout << System::String::Format(u"Pattern value is: {0}", fill->get_Pattern()) << std::endl;

// هناك عدة طرق لتحديد تعبئة بنمط.
// 1 -  تطبيق النمط على تعبئة الشكل:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick);

// 2 -  تطبيق النمط مع ألوان المقدمة والخلفية على تعبئة الشكل:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick, System::Drawing::Color::get_Aqua(), System::Drawing::Color::get_Bisque());

doc->Save(get_ArtifactsDir() + u"Shape.FillPattern.docx");
```

## انظر أيضًا

* Enum [PatternType](../../patterntype/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## Fill::Patterned(Aspose::Words::Drawing::PatternType, System::Drawing::Color, System::Drawing::Color) method


يضبط التعبئة المحددة لتصبح نمطًا.

```cpp
void Aspose::Words::Drawing::Fill::Patterned(Aspose::Words::Drawing::PatternType patternType, System::Drawing::Color foreColor, System::Drawing::Color backColor)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| patternType | Aspose::Words::Drawing::PatternType | [PatternType](../../patterntype/) |
| foreColor | System::Drawing::Color | لون التعبئة الأمامية. |
| backColor | System::Drawing::Color | لون تعبئة الخلفية. |

## أمثلة



يوضح كيفية تعيين نمط لشكل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();

std::cout << System::String::Format(u"Pattern value is: {0}", fill->get_Pattern()) << std::endl;

// هناك عدة طرق لتحديد تعبئة بنمط.
// 1 -  تطبيق النمط على تعبئة الشكل:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick);

// 2 -  تطبيق النمط مع ألوان المقدمة والخلفية على تعبئة الشكل:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick, System::Drawing::Color::get_Aqua(), System::Drawing::Color::get_Bisque());

doc->Save(get_ArtifactsDir() + u"Shape.FillPattern.docx");
```

## انظر أيضًا

* Enum [PatternType](../../patterntype/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
