---
title: "Aspose::Words::DocumentBuilder::InsertShape Methode"
linktitle: "InsertShape"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::InsertShape Methode. Fügt eine frei schwebende Form mit angegebenen Position, Größe und Textumbruchtyp in C++ ein."
type: docs
weight: 45000
url: /de/cpp/aspose.words/documentbuilder/insertshape/
---
## DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Fügt eine frei schwebende Form mit angegebener Position, Größe und Textumbruchtyp ein.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType shapeType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| shapeType | Aspose::Words::Drawing::ShapeType | Der Formtyp, der in das Dokument eingefügt werden soll |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Gibt an, von wo aus der horizontale Abstand zur Form gemessen wird. |
| left | double | Abstand in Punkten vom Ursprung zur linken Seite der Form. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Gibt an, von wo aus der vertikale Abstand zur Form gemessen wird. |
| top | double | Abstand in Punkten vom Ursprung zur oberen Seite der Form. |
| Breite | double | Die Breite der Form in Punkten. |
| Höhe | double | Die Höhe der Form in Punkten. |
| wrapType | Aspose::Words::Drawing::WrapType | Gibt an, wie Text um die Form gewickelt wird. |

### ReturnValue

Der eingefügte Formknoten.

## Beispiele



Zeigt, wie man DML‑Formen in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Unten sind zwei Umbruchtypen aufgeführt, die Formen haben können.
// 1 -  Schwebend:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::TopCornersRounded, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 100, 50, 50, Aspose::Words::Drawing::WrapType::None);

// 2 -  Eingebettet:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::DiagonalCornersRounded, 50, 50);

// Wenn Sie "non-primitive"‑Formen erstellen müssen, wie SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded oder DiagonalCornersRounded,
// speichern Sie das Dokument dann mit "Strict"‑ oder "Transitional"‑Compliance, was das Speichern der Form als DML ermöglicht.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeInsertion.docx", saveOptions);
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType, double, double) method


Fügt eine Inline‑Form mit angegebenem Typ und Größe ein.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType shapeType, double width, double height)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| shapeType | Aspose::Words::Drawing::ShapeType | Der Formtyp, der in das Dokument eingefügt werden soll. |
| Breite | double | Die Breite der Form in Punkten. |
| Höhe | double | Die Höhe der Form in Punkten. |

### ReturnValue

Der eingefügte Formknoten.

## Beispiele



Zeigt, wie man DML‑Formen in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Unten sind zwei Umbruchtypen aufgeführt, die Formen haben können.
// 1 -  Schwebend:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::TopCornersRounded, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 100, 50, 50, Aspose::Words::Drawing::WrapType::None);

// 2 -  Eingebettet:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::DiagonalCornersRounded, 50, 50);

// Wenn Sie "non-primitive"‑Formen erstellen müssen, wie SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded oder DiagonalCornersRounded,
// speichern Sie das Dokument dann mit "Strict"‑ oder "Transitional"‑Compliance, was das Speichern der Form als DML ermöglicht.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeInsertion.docx", saveOptions);
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
