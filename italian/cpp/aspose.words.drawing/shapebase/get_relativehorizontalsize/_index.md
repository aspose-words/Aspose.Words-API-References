---
title: "Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize metodo"
linktitle: "get_RelativeHorizontalSize"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize metodo. Ottiene o imposta il valore della dimensione relativa della shape nella direzione orizzontale in C++."
type: docs
weight: 42500
url: /it/cpp/aspose.words.drawing/shapebase/get_relativehorizontalsize/
---
## ShapeBase::get_RelativeHorizontalSize method


Ottiene o imposta il valore della dimensione relativa della forma nella direzione orizzontale.

```cpp
Aspose::Words::Drawing::RelativeHorizontalSize Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize()
```

## Note


Il valore predefinito è [RelativeHorizontalSize](../../relativehorizontalsize/).

Ha effetto solo se [WidthRelative](../get_widthrelative/) è impostato.

## Esempi



Mostra come impostare la dimensione e la posizione relative.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aggiunta di una forma semplice con dimensione e posizione assolute.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 40);
// Imposta WrapType su WrapType.None poiché le forme Inline vengono convertite automaticamente in unità assolute.
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Verifica e impostazione della dimensione orizzontale relativa.
if (shape->get_RelativeHorizontalSize() == Aspose::Words::Drawing::RelativeHorizontalSize::Default)
{
    // Impostazione del vincolo della dimensione orizzontale su Margin.
    shape->set_RelativeHorizontalSize(Aspose::Words::Drawing::RelativeHorizontalSize::Margin);
    // Impostazione della larghezza al 50% della larghezza di Margin.
    shape->set_WidthRelative(50.0f);
}

// Verifica e impostazione della dimensione verticale relativa.
if (shape->get_RelativeVerticalSize() == Aspose::Words::Drawing::RelativeVerticalSize::Default)
{
    // Impostazione del vincolo della dimensione verticale su Margin.
    shape->set_RelativeVerticalSize(Aspose::Words::Drawing::RelativeVerticalSize::Margin);
    // Impostazione dell'heigh al 30% dell'altezza di Margin.
    shape->set_HeightRelative(30.0f);
}

// Verifica e impostazione della posizione verticale relativa.
if (shape->get_RelativeVerticalPosition() == Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph)
{
    // etting il vincolo della posizione su TopMargin.
    shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin);
    // Impostazione di Top relativo al 30% della posizione di TopMargin.
    shape->set_TopRelative(30.0f);
}

// Verifica e impostazione della posizione orizzontale relativa.
if (shape->get_RelativeHorizontalPosition() == Aspose::Words::Drawing::RelativeHorizontalPosition::Default)
{
    // Impostazione del vincolo della posizione su RightMargin.
    shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin);
    // Il valore relativo della posizione può essere negativo.
    shape->set_LeftRelative(-260.0f);
}

doc->Save(get_ArtifactsDir() + u"Shape.RelativeSizeAndPosition.docx");
```

## Vedi anche

* Enum [RelativeHorizontalSize](../../relativehorizontalsize/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
