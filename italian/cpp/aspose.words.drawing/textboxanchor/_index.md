---
title: "Aspose::Words::Drawing::TextBoxAnchor enum"
linktitle: "TextBoxAnchor"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::TextBoxAnchor enum. Specifica i valori usati per l'allineamento verticale del testo della forma in C++."
type: docs
weight: 39000
url: /it/cpp/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enum


Specifica i valori utilizzati per l'allineamento verticale del testo nella forma.

```cpp
enum class TextBoxAnchor
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Superiore | 0 | Il testo è allineato alla parte superiore della casella di testo. |
| Middle | 1 | Il testo è allineato al centro della casella di testo. |
| Inferiore | 2 | Il testo è allineato alla parte inferiore della casella di testo. |
| TopCentered | 3 | Il testo è allineato al centro superiore della casella di testo. |
| MiddleCentered | 4 | Il testo è allineato al centro medio della casella di testo. |
| BottomCentered | 5 | Il testo è allineato al centro inferiore della casella di testo. |
| TopBaseline | 6 | Il testo è allineato alla linea di base superiore della casella di testo. |
| BottomBaseline | 7 | Il testo è allineato alla linea di base inferiore della casella di testo. |
| TopCenteredBaseline | 8 | Il testo è allineato alla linea di base centrata superiore della casella di testo. |
| BottomCenteredBaseline | 9 | Il testo è allineato alla linea di base centrata inferiore della casella di testo. |


## Esempi



Mostra come allineare verticalmente il contenuto testuale di una casella di testo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 200, 200);

// Imposta la proprietà "VerticalAnchor" su "TextBoxAnchor.Top" per
// allineare il testo in questa casella di testo al lato superiore della forma.
// Imposta la proprietà "VerticalAnchor" su "TextBoxAnchor.Middle" per
// allineare il testo in questa casella di testo al centro della forma.
// Imposta la proprietà "VerticalAnchor" su "TextBoxAnchor.Bottom" per
// allineare il testo in questa casella di testo al fondo della forma.
shape->get_TextBox()->set_VerticalAnchor(verticalAnchor);

builder->MoveTo(shape->get_FirstParagraph());
builder->Write(u"Hello world!");

// L'allineamento verticale del testo all'interno delle caselle di testo è disponibile da Microsoft Word 2007 in poi.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2007);
doc->Save(get_ArtifactsDir() + u"Shape.VerticalAnchor.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
