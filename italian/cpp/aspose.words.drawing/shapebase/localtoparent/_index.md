---
title: "Metodo LocalToParent di Aspose::Words::Drawing::ShapeBase"
linktitle: "LocalToParent"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo LocalToParent di Aspose::Words::Drawing::ShapeBase. Converte un valore dallo spazio di coordinate locale nello spazio di coordinate della forma genitore in C++."
type: docs
weight: 61000
url: /it/cpp/aspose.words.drawing/shapebase/localtoparent/
---
## ShapeBase::LocalToParent method


Converte un valore dallo spazio di coordinate locale allo spazio di coordinate della forma genitore.

```cpp
System::Drawing::PointF Aspose::Words::Drawing::ShapeBase::LocalToParent(System::Drawing::PointF value)
```


## Esempi



Mostra come tradurre la posizione delle coordinate x e y sul piano di coordinate di una forma in una posizione sul piano di coordinate della forma genitore.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Inserisci una forma di gruppo e posizionala 100 punti sotto e a destra di
// il punto di origine delle coordinate x e Y del documento.
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(100.0f, 100.0f, 500.0f, 500.0f));

// Usa il metodo "LocalToParent" per determinare che (0, 0) sulle coordinate interne x e y del gruppo
// si trovi su (100, 100) del sistema di coordinate della sua forma genitore. Il genitore della forma di gruppo è il documento stesso.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(100.0f, 100.0f), group->LocalToParent(System::Drawing::PointF(0.0f, 0.0f)));

// Per impostazione predefinita, il piano di coordinate interno di una forma ha l'angolo in alto a sinistra a (0, 0),
// e l'angolo in basso a destra a (1000, 1000). A causa delle sue dimensioni, la nostra forma di gruppo copre un'area di 500pt x 500pt
// nel piano del documento. Ciò significa che un movimento di 1pt sul piano di coordinate del documento verrà tradotto
// in un movimento di 2pt sul piano di coordinate della forma di gruppo.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(150.0f, 150.0f), group->LocalToParent(System::Drawing::PointF(100.0f, 100.0f)));
ASPOSE_ASSERT_EQ(System::Drawing::PointF(200.0f, 200.0f), group->LocalToParent(System::Drawing::PointF(200.0f, 200.0f)));
ASPOSE_ASSERT_EQ(System::Drawing::PointF(250.0f, 250.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Sposta l'origine degli assi x e y della forma di gruppo dall'angolo in alto a sinistra al centro.
// Ciò sposterà ulteriormente le coordinate interne del gruppo rispetto alle coordinate del documento.
group->set_CoordOrigin(System::Drawing::Point(-250, -250));

ASPOSE_ASSERT_EQ(System::Drawing::PointF(375.0f, 375.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Modificare la scala del piano di coordinate influenzerà anche le posizioni relative.
group->set_CoordSize(System::Drawing::Size(500, 500));

ASPOSE_ASSERT_EQ(System::Drawing::PointF(650.0f, 650.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Se desideriamo aggiungere una forma a questo gruppo definendo la sua posizione in base a una posizione nel documento,
// dovremo prima confermare una posizione nella forma di gruppo che corrisponda alla posizione del documento.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(700.0f, 700.0f), group->LocalToParent(System::Drawing::PointF(350.0f, 350.0f)));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(700);
shape->set_Top(700);

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::GroupShape>>(group);

doc->Save(get_ArtifactsDir() + u"Shape.LocalToParent.docx");
```

## Vedi anche

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
