---
title: "Metodo Aspose::Words::Drawing::ShapeBase::get_Font"
linktitle: "get_Font"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::ShapeBase::get_Font. Fornisce l'accesso alla formattazione del carattere di questo oggetto in C++."
type: docs
weight: 21000
url: /it/cpp/aspose.words.drawing/shapebase/get_font/
---
## ShapeBase::get_Font method


Fornisce l'accesso alla formattazione del carattere di questo oggetto.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Drawing::ShapeBase::get_Font()
```


## Esempi



Mostra come inserire una casella di testo e impostare il carattere del suo contenuto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 50);
builder->MoveTo(shape->get_LastParagraph());
builder->Write(u"This text is inside the text box.");

// Imposta la proprietà "Hidden" dell'oggetto "Font" della forma su "true" per nascondere la casella di testo dalla vista
// e comprimi lo spazio che occuperebbe normalmente.
// Imposta la proprietà "Hidden" dell'oggetto "Font" della forma su "false" per lasciare la casella di testo visibile.
shape->get_Font()->set_Hidden(hideShape);

// Se la forma è visibile, modificheremo il suo aspetto tramite l'oggetto font.
if (!hideShape)
{
    shape->get_Font()->set_HighlightColor(System::Drawing::Color::get_LightGray());
    shape->get_Font()->set_Color(System::Drawing::Color::get_Red());
    shape->get_Font()->set_Underline(Aspose::Words::Underline::Dash);
}

// Sposta il builder fuori dalla casella di testo e riportalo nel documento principale.
builder->MoveTo(shape->get_ParentParagraph());

builder->Writeln(u"\nThis text is outside the text box.");

doc->Save(get_ArtifactsDir() + u"Shape.Font.docx");
```

## Vedi anche

* Class [Font](../../../aspose.words/font/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
