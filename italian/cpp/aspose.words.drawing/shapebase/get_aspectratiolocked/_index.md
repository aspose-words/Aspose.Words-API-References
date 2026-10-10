---
title: "Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked metodo"
linktitle: "get_AspectRatioLocked"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked metodo. Specifica se il rapporto d'aspetto della shape''s è bloccato in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.drawing/shapebase/get_aspectratiolocked/
---
## ShapeBase::get_AspectRatioLocked method


Specifica se il rapporto d'aspetto della forma è bloccato.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked()
```

## Note


Il valore predefinito dipende da [ShapeType](../../shapetype/), per [Image](../../shapetype/) è **true** ma per gli altri tipi di forma è **false**.

Ha effetto solo per le forme di livello superiore.

## Esempi



Mostra come bloccare/sbloccare il rapporto d'aspetto di una forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci una forma. Se apriamo questo documento in Microsoft Word, possiamo fare clic sinistro sulla forma per rivelare
// otto maniglie di ridimensionamento intorno al suo perimetro, che possiamo cliccare e trascinare per cambiarne le dimensioni.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Imposta la proprietà \"AspectRatioLocked\" su \"true\" per preservare il rapporto d'aspetto della forma
// quando si usano le quattro maniglie di ridimensionamento diagonali, che modificano sia l'altezza che la larghezza dell'immagine.
// L'uso di qualsiasi maniglia di ridimensionamento ortogonale che modifichi l'altezza o la larghezza cambierà comunque il rapporto d'aspetto.
// Imposta la proprietà \"AspectRatioLocked\" su \"false\" per consentirci di
// cambiare liberamente il rapporto d'aspetto dell'immagine con tutte le maniglie di ridimensionamento.
shape->set_AspectRatioLocked(lockAspectRatio);

doc->Save(get_ArtifactsDir() + u"Shape.AspectRatio.docx");
```

## Vedi anche

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
