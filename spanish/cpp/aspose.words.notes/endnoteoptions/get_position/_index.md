---
title: "Aspose::Words::Notes::EndnoteOptions::get_Position método"
linktitle: "get_Position"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Notes::EndnoteOptions::get_Position método. Especifica la posición de las notas al final en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.notes/endnoteoptions/get_position/
---
## EndnoteOptions::get_Position method


Especifica la posición de las notas finales.

```cpp
Aspose::Words::Notes::EndnotePosition Aspose::Words::Notes::EndnoteOptions::get_Position()
```


## Ejemplos



Muestra cómo seleccionar un lugar diferente donde el documento recopila y muestra sus notas finales.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Una nota final es una forma de adjuntar una referencia o un comentario marginal al texto
// que no interfiere con el flujo del texto principal.
// Insertar una nota al final agrega un pequeño símbolo de referencia en superíndice
// en el texto principal donde insertamos la nota al final.
// Cada nota al final también crea una entrada al final del documento, que consiste en un símbolo
// que coincide con el símbolo de referencia en el texto principal.
// El texto de referencia que pasamos al método "InsertEndnote" del constructor de documentos.
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote contents.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"This is the second section.");

// Podemos usar la propiedad "Position" para determinar dónde colocará el documento todas sus notas al final.
// Si establecemos el valor de la propiedad "Position" a "EndnotePosition.EndOfDocument",
// cada nota al pie aparecerá en una colección al final del documento. Este es el valor predeterminado.
// Si establecemos el valor de la propiedad "Position" a "EndnotePosition.EndOfSection",
// cada nota al pie aparecerá en una colección al final de la sección cuyo texto contiene la marca de referencia de la nota al final.
doc->get_EndnoteOptions()->set_Position(endnotePosition);

doc->Save(get_ArtifactsDir() + u"InlineStory.PositionEndnote.docx");
```

## Ver también

* Enum [EndnotePosition](../../endnoteposition/)
* Class [EndnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
