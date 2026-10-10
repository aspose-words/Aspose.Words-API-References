---
title: "Metodo Aspose::Words::Drawing::ShapeBase::get_BoundsInPoints"
linktitle: "get_BoundsInPoints"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::ShapeBase::get_BoundsInPoints. Ottiene la posizione e le dimensioni del blocco contenitore della forma in punti, relativo all'ancora della forma più in alto in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.drawing/shapebase/get_boundsinpoints/
---
## ShapeBase::get_BoundsInPoints method


Ottiene la posizione e le dimensioni del blocco contenitore della forma in punti, relative all'ancora della forma più in alto.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::get_BoundsInPoints()
```


## Esempi



Mostra come verificare i confini del blocco contenitore della forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Line, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 50, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 50, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->set_StrokeColor(System::Drawing::Color::get_Orange());

// Anche se la linea stessa occupa poco spazio nella pagina del documento,
// occupa un blocco contenitore rettangolare, la cui dimensione possiamo determinare usando le proprietà "Bounds".
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(50.0f, 50.0f, 100.0f, 100.0f), shape->get_Bounds());
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(50.0f, 50.0f, 100.0f, 100.0f), shape->get_BoundsInPoints());

// Crea una forma di gruppo, quindi imposta la dimensione del suo blocco contenitore usando la proprietà "Bounds".
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f));

ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f), group->get_BoundsInPoints());

// Crea un rettangolo, verifica la dimensione del suo blocco di delimitazione, e poi aggiungilo alla forma di gruppo.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(700);
shape->set_Top(700);

ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(700.0f, 700.0f, 100.0f, 100.0f), shape->get_BoundsInPoints());

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Il piano di coordinate della forma di gruppo ha la sua origine nell'angolo in alto a sinistra del suo blocco contenitore,
// e le coordinate x e y di (1000, 1000) nell'angolo in basso a destra.
// La nostra forma di gruppo misura 250x250pt, quindi ogni 4pt sul piano di coordinate della forma di gruppo
// corrisponde a 1pt nel piano di coordinate del corpo del documento.
// Ogni forma che inseriamo si ridurrà inoltre di dimensione di un fattore 4.
// La modifica nella proprietà "BoundsInPoints" della forma rifletterà questo.
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(175.0f, 275.0f, 25.0f, 25.0f), shape->get_BoundsInPoints());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::GroupShape>>(group);

// Inserisci una forma e posizionala al di fuori dei limiti del blocco contenitore della forma di gruppo.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(1000);
shape->set_Top(1000);

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// L'impronta della forma di gruppo nel corpo del documento è aumentata, ma il blocco contenitore rimane lo stesso.
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f), group->get_BoundsInPoints());
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(250.0f, 350.0f, 25.0f, 25.0f), shape->get_BoundsInPoints());

doc->Save(get_ArtifactsDir() + u"Shape.Bounds.docx");
```

## Vedi anche

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
