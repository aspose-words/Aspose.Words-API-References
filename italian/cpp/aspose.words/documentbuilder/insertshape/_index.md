---
title: "Aspose::Words::DocumentBuilder::InsertShape method"
linktitle: "InsertShape"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBuilder::InsertShape method. Inserisce una forma fluttuante con posizione, dimensione e tipo di avvolgimento del testo specificati in C++."
type: docs
weight: 45000
url: /it/cpp/aspose.words/documentbuilder/insertshape/
---
## DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Inserisce una forma fluttuante con posizione, dimensione e tipo di avvolgimento del testo specificati.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType shapeType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| shapeType | Aspose::Words::Drawing::ShapeType | Il tipo di forma da inserire nel documento |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Specifica da dove viene misurata la distanza orizzontale alla forma. |
| left | double | Distanza in punti dall'origine al lato sinistro della forma. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Specifica da dove si misura la distanza verticale alla forma. |
| superiore | double | Distanza in punti dall'origine al lato superiore della forma. |
| larghezza | double | La larghezza della forma in punti. |
| altezza | double | L'altezza della forma in punti. |
| wrapType | Aspose::Words::Drawing::WrapType | Specifica come avvolgere il testo attorno alla forma. |

### ReturnValue

Il nodo della forma che è stato inserito.

## Esempi



Mostra come inserire forme DML in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Di seguito sono riportati due tipi di avvolgimento che le forme possono avere.
// 1 -  Fluttuante:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::TopCornersRounded, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 100, 50, 50, Aspose::Words::Drawing::WrapType::None);

// 2 -  In linea:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::DiagonalCornersRounded, 50, 50);

// Se è necessario creare forme "non-primitive", come SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, o DiagonalCornersRounded,
// quindi salva il documento con conformità "Strict" o "Transitional", che consente di salvare la forma come DML.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeInsertion.docx", saveOptions);
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType, double, double) method


Inserisce una forma in linea con tipo e dimensione specificati.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType shapeType, double width, double height)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| shapeType | Aspose::Words::Drawing::ShapeType | Il tipo di forma da inserire nel documento. |
| larghezza | double | La larghezza della forma in punti. |
| altezza | double | L'altezza della forma in punti. |

### ReturnValue

Il nodo della forma che è stato inserito.

## Esempi



Mostra come inserire forme DML in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Di seguito sono riportati due tipi di avvolgimento che le forme possono avere.
// 1 -  Fluttuante:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::TopCornersRounded, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 100, 50, 50, Aspose::Words::Drawing::WrapType::None);

// 2 -  In linea:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::DiagonalCornersRounded, 50, 50);

// Se è necessario creare forme "non-primitive", come SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, o DiagonalCornersRounded,
// quindi salva il documento con conformità "Strict" o "Transitional", che consente di salvare la forma come DML.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeInsertion.docx", saveOptions);
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
