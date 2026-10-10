---
title: "Aspose::Words::Notes::FootnoteOptions::get_Position método"
linktitle: "get_Position"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Notes::FootnoteOptions::get_Position método. Especifica la posición de las notas al pie en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.notes/footnoteoptions/get_position/
---
## FootnoteOptions::get_Position method


Especifica la posición de las notas al pie.

```cpp
Aspose::Words::Notes::FootnotePosition Aspose::Words::Notes::FootnoteOptions::get_Position()
```


## Ejemplos



Muestra cómo seleccionar un lugar diferente donde el documento recopila y muestra sus notas al pie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Una nota al pie es una forma de adjuntar una referencia o un comentario al texto.
// que no interfiere con el flujo del texto principal.
// Insertar una nota al pie agrega un pequeño símbolo de referencia en superíndice.
// en el texto principal donde insertamos la nota al pie.
// Cada nota al pie también crea una entrada al final de la página, que consiste en un símbolo
// que coincide con el símbolo de referencia en el texto principal.
// El texto de referencia que pasamos al método "InsertFootnote" del generador de documentos.
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote contents.");

// Podemos usar la propiedad "Position" para determinar dónde el documento colocará todas sus notas al pie.
// Si establecemos el valor de la propiedad "Position" a "FootnotePosition.BottomOfPage",
// cada nota al pie aparecerá al final de la página que contiene su marca de referencia. Este es el valor predeterminado.
// Si establecemos el valor de la propiedad "Position" a "FootnotePosition.BeneathText",
// cada nota al pie aparecerá al final del texto de la página que contiene su marca de referencia.
doc->get_FootnoteOptions()->set_Position(footnotePosition);

doc->Save(get_ArtifactsDir() + u"InlineStory.PositionFootnote.docx");
```

## Ver también

* Enum [FootnotePosition](../../footnoteposition/)
* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
