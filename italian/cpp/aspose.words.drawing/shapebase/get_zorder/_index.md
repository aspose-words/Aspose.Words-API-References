---
title: "Metodo Aspose::Words::Drawing::ShapeBase::get_ZOrder"
linktitle: "get_ZOrder"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::ShapeBase::get_ZOrder. Determina l'ordine di visualizzazione delle forme sovrapposte in C++."
type: docs
weight: 57000
url: /it/cpp/aspose.words.drawing/shapebase/get_zorder/
---
## ShapeBase::get_ZOrder method


Determina l'ordine di visualizzazione delle forme sovrapposte.

```cpp
int32_t Aspose::Words::Drawing::ShapeBase::get_ZOrder()
```

## Note


Ha effetto solo per le forme di livello superiore.

Il valore predefinito è 0.

Il numero rappresenta la precedenza di impilamento. Una forma con un numero più alto verrà visualizzata come se fosse sovrapposta ("davanti a") una forma con un numero più basso.

L'ordine delle forme sovrapposte è indipendente per le forme nell'intestazione e nel testo principale del documento.

L'ordine di visualizzazione delle forme figlie in una forma di gruppo è determinato dal loro ordine all'interno del gruppo.

## Esempi



Mostra come manipolare l'ordine delle forme.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci tre rettangoli di colore diverso che si sovrappongono parzialmente.
// Quando inseriamo una forma che sovrappone un'altra forma, Aspose.Words posiziona la forma più recente sopra quella più vecchia.
// Il rettangolo verde chiaro sovrapporrà il rettangolo blu chiaro e lo oscurerà parzialmente,
// e il rettangolo blu chiaro oscurerà il rettangolo arancione.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_Orange());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 150, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 150, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 200, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 200, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_LightGreen());

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

// La proprietà "ZOrder" di una forma determina la sua priorità di impilamento rispetto alle altre forme sovrapposte.
// Se due forme sovrapposte hanno valori "ZOrder" diversi,
// Microsoft Word posizionerà la forma con valore più alto sopra la forma con valore più basso.
// Imposta i valori "ZOrder" delle nostre forme per posizionare il primo rettangolo arancione sopra il secondo rettangolo blu chiaro
// e il secondo rettangolo blu chiaro sopra il terzo rettangolo verde chiaro.
// Questo invertirà il loro ordine di impilamento originale.
shapes[0]->set_ZOrder(3);
shapes[1]->set_ZOrder(2);
shapes[2]->set_ZOrder(1);

doc->Save(get_ArtifactsDir() + u"Shape.ZOrder.docx");
```

## Vedi anche

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
