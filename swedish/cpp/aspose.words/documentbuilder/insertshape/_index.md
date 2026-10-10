---
title: "Aspose::Words::DocumentBuilder::InsertShape metod"
linktitle: "InsertShape"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::InsertShape metod. Infogar en fristående form med angiven position, storlek och textomslagnings‑typ i C++."
type: docs
weight: 45000
url: /sv/cpp/aspose.words/documentbuilder/insertshape/
---
## DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Infogar en fristående form med angiven position, storlek och typ av textomslag.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType shapeType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| shapeType | Aspose::Words::Drawing::ShapeType | Formtypen att infoga i dokumentet |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Anger var det horisontella avståndet till formen mäts från. |
| left | double | Avstånd i punkter från ursprunget till formens vänstra sida. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Anger var det vertikala avståndet till formen mäts från. |
| top | double | Avstånd i punkter från ursprunget till formens övre sida. |
| bredd | double | Formens bredd i punkter. |
| höjd | double | Formens höjd i punkter. |
| wrapType | Aspose::Words::Drawing::WrapType | Anger hur texten omsluter formen. |

### ReturnValue

Formnod som infogades.

## Exempel



Visar hur man infogar DML-former i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nedan är två omslagstyper som former kan ha.
// 1 -  Flytande:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::TopCornersRounded, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 100, 50, 50, Aspose::Words::Drawing::WrapType::None);

// 2 -  Inbäddad:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::DiagonalCornersRounded, 50, 50);

// Om du behöver skapa \"icke-primitive\" former, såsom SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, eller DiagonalCornersRounded,
// spara sedan dokumentet med \"Strict\" eller \"Transitional\"-kompatibilitet, vilket tillåter att spara formen som DML.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeInsertion.docx", saveOptions);
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType, double, double) method


Infogar en inline-form med angiven typ och storlek.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType shapeType, double width, double height)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| shapeType | Aspose::Words::Drawing::ShapeType | Formtypen att infoga i dokumentet. |
| bredd | double | Formens bredd i punkter. |
| höjd | double | Formens höjd i punkter. |

### ReturnValue

Formnod som infogades.

## Exempel



Visar hur man infogar DML-former i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nedan är två omslagstyper som former kan ha.
// 1 -  Flytande:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::TopCornersRounded, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 100, 50, 50, Aspose::Words::Drawing::WrapType::None);

// 2 -  Inbäddad:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::DiagonalCornersRounded, 50, 50);

// Om du behöver skapa \"icke-primitive\" former, såsom SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, eller DiagonalCornersRounded,
// spara sedan dokumentet med \"Strict\" eller \"Transitional\"-kompatibilitet, vilket tillåter att spara formen som DML.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeInsertion.docx", saveOptions);
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
