---
title: "Aspose::Words::Drawing::TextBox::get_VerticalAnchor metodo"
linktitle: "get_VerticalAnchor"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::TextBox::get_VerticalAnchor metodo. Specifica l'allineamento verticale del testo all'interno di una forma in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words.drawing/textbox/get_verticalanchor/
---
## TextBox::get_VerticalAnchor method


Specifica l'allineamento verticale del testo all'interno di una forma.

```cpp
Aspose::Words::Drawing::TextBoxAnchor Aspose::Words::Drawing::TextBox::get_VerticalAnchor()
```

## Note


Il valore predefinito è [Top](../../textboxanchor/).

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

* Enum [TextBoxAnchor](../../textboxanchor/)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
