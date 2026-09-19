---
title: "Aspose::Words::DocumentBuilder::get_CurrentSection metodo"
linktitle: "get_CurrentSection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBuilder::get_CurrentSection metodo. Ottiene la sezione attualmente selezionata in questo DocumentBuilder in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words/documentbuilder/get_currentsection/
---
## DocumentBuilder::get_CurrentSection method


Ottiene la sezione attualmente selezionata in questo [DocumentBuilder](../).

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::DocumentBuilder::get_CurrentSection()
```


## Esempi



Mostra come inserire un'immagine flottante e specificarne la posizione e le dimensioni.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Configura la proprietà "RelativeHorizontalPosition" della forma per trattare il valore della proprietà "Left"
// come distanza orizzontale della forma, in punti, dal lato sinistro della pagina.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);

// Imposta la distanza orizzontale della forma dal lato sinistro della pagina a 100.
shape->set_Left(100);

// Usa la proprietà "RelativeVerticalPosition" in modo simile per posizionare la forma 80pt sotto la parte superiore della pagina.
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Top(80);

// Imposta l'altezza della forma, che scalerà automaticamente la larghezza per preservare le dimensioni.
shape->set_Height(125);

ASPOSE_ASSERT_EQ(125.0, shape->get_Width());

// Le proprietà "Bottom" e "Right" contengono i bordi inferiore e destro dell'immagine.
ASPOSE_ASSERT_EQ(shape->get_Top() + shape->get_Height(), shape->get_Bottom());
ASPOSE_ASSERT_EQ(shape->get_Left() + shape->get_Width(), shape->get_Right());

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPositionSize.docx");
```

## Vedi anche

* Class [Section](../../section/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
