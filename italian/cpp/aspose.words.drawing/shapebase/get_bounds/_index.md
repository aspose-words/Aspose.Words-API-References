---
title: "Metodo Aspose::Words::Drawing::ShapeBase::get_Bounds"
linktitle: "get_Bounds"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::ShapeBase::get_Bounds. Ottiene o imposta la posizione e le dimensioni del blocco contenitore della forma in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.drawing/shapebase/get_bounds/
---
## ShapeBase::get_Bounds method


Ottiene o imposta la posizione e le dimensioni del blocco contenitore della forma.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::get_Bounds()
```

## Note


Ignora il blocco del rapporto di aspetto durante l'impostazione.

Per una forma di livello superiore, il valore è in punti e relativo all'ancora della forma.

Per le forme in un gruppo, il valore è nello spazio delle coordinate e nelle unità del gruppo genitore.

## Esempi



Mostra come creare e popolare una forma di gruppo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Crea una forma di gruppo. Una forma di gruppo può visualizzare una collezione di nodi di forme figlie.
// In Microsoft Word, facendo clic all'interno del contorno della forma di gruppo o su una delle forme figlie della forma di gruppo,
// selezionerà tutte le altre forme figlie all'interno di questo gruppo e ci permetterà di scalare e spostare tutte le forme contemporaneamente.
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);

ASSERT_EQ(Aspose::Words::Drawing::WrapType::None, group->get_WrapType());

// Crea una forma di gruppo di 400pt x 400pt e posizionala all'origine delle coordinate della forma fluttuante del documento.
group->set_Bounds(System::Drawing::RectangleF(0.0f, 0.0f, 400.0f, 400.0f));

// Imposta la dimensione del piano di coordinate interno del gruppo a 500 x 500pt.
// L'angolo in alto a sinistra del gruppo avrà una coordinata x e y di (0, 0),
// e l'angolo in basso a destra avrà una coordinata x e y di (500, 500).
group->set_CoordSize(System::Drawing::Size(500, 500));

// Imposta le coordinate dell'angolo in alto a sinistra del gruppo a (-250, -250).
// Il centro del gruppo avrà ora un valore di coordinata x e y di (0, 0),
// e l'angolo in basso a destra sarà a (250, 250).
group->set_CoordOrigin(System::Drawing::Point(-250, -250));

// Crea un rettangolo che visualizzerà il contorno di questa forma di gruppo e aggiungilo al gruppo.
auto child1 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
child1->set_Width(group->get_CoordSize().get_Width());
child1->set_Height(group->get_CoordSize().get_Height());
child1->set_Left(group->get_CoordOrigin().get_X());
child1->set_Top(group->get_CoordOrigin().get_Y());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child1);

// Una volta che una forma fa parte di una forma di gruppo, possiamo accedervi come nodo figlio e poi modificarla.
(System::ExplicitCast<Aspose::Words::Drawing::Shape>(group->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Stroke()->set_DashStyle(Aspose::Words::Drawing::DashStyle::Dash);

// Crea una piccola stella rossa e inseriscila nel gruppo.
// Allinea la forma con l'origine delle coordinate del gruppo, che abbiamo spostato al centro.
auto child2 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Star);
child2->set_Width(20);
child2->set_Height(20);
child2->set_Left(-10);
child2->set_Top(-10);
child2->set_FillColor(System::Drawing::Color::get_Red());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child2);

// Inserisci un rettangolo, e poi inserisci un rettangolo leggermente più piccolo nello stesso punto con un'immagine.
// Le forme più recenti che aggiungiamo al gruppo si sovrappongono alle forme più vecchie. Il rettangolo azzurro chiaro si sovrapporrà parzialmente alla stella rossa,
// e poi la forma con l'immagine si sovrapporrà al rettangolo azzurro chiaro, usandolo come cornice.
// Non possiamo usare le proprietà "ZOrder" delle forme per manipolare il loro ordine all'interno di una forma di gruppo.
auto child3 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
child3->set_Width(250);
child3->set_Height(250);
child3->set_Left(-250);
child3->set_Top(-250);
child3->set_FillColor(System::Drawing::Color::get_LightBlue());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child3);

auto child4 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
child4->set_Width(200);
child4->set_Height(200);
child4->set_Left(-225);
child4->set_Top(-225);
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child4);

(System::ExplicitCast<Aspose::Words::Drawing::Shape>(group->GetChild(Aspose::Words::NodeType::Shape, 3, true)))->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Inserisci una casella di testo nella forma di gruppo. Imposta la proprietà "Left" in modo che il bordo destro della casella di testo
// tocchi il confine destro della forma di gruppo. Imposta la proprietà "Top" in modo che la casella di testo si trovi al di fuori
// del confine della forma di gruppo, con la sua parte superiore allineata lungo il margine inferiore della forma di gruppo.
auto child5 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
child5->set_Width(200);
child5->set_Height(50);
child5->set_Left(group->get_CoordSize().get_Width() + group->get_CoordOrigin().get_X() - 200);
child5->set_Top(group->get_CoordSize().get_Height() + group->get_CoordOrigin().get_Y());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child5);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(group);
builder->MoveTo((System::ExplicitCast<Aspose::Words::Drawing::Shape>(group->GetChild(Aspose::Words::NodeType::Shape, 4, true)))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"Shape.GroupShape.docx");
```


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
