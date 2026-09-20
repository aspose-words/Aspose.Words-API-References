---
title: "Aspose::Words::Notes::FootnoteType enum"
linktitle: "FootnoteType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Notes::FootnoteType enum. Especifica si se trata de una nota al pie o una nota final en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.notes/footnotetype/
---
## FootnoteType enum


Especifica si se trata de una nota al pie o una nota final.

```cpp
enum class FootnoteType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Footnote | 0 | El objeto es una nota al pie. |
| Nota final | 1 | El objeto es una nota final. |

## Observaciones


Tanto las notas al pie como las notas finales están representadas por objetos mediante la clase [Footnote](./). Use [FootnoteType](../footnote/get_footnotetype/) para distinguir entre notas al pie y notas finales.

## Ejemplos



Muestra cómo referenciar texto con una nota al pie y una nota final.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte algún texto y márquelo con una nota al pie con la propiedad IsAuto establecida en "true" por defecto,
// de modo que el marcador visto en el texto principal será numerado automáticamente como "1",
// y la nota al pie aparecerá al final de la página.
builder->Write(u"This text will be referenced by a footnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote comment regarding referenced text.");

// Inserte más texto y márquelo con una nota final con una marca de referencia personalizada,
// que se usará en lugar del número "2" y establecerá "IsAuto" a false.
builder->Write(u"This text will be referenced by an endnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote comment regarding referenced text.", u"CustomMark");

// Las notas al pie siempre aparecen al final del texto al que hacen referencia,
// por lo que este salto de página no afectará a la nota al pie.
// Por otro lado, las notas finales siempre están al final del documento
// de modo que este salto de página empujará la nota final a la página siguiente.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFootnote.docx");
```


Muestra cómo insertar y personalizar notas al pie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Agregue texto y refiérelo con una nota al pie. Esta nota al pie colocará una pequeña referencia en superíndice
// después del texto al que hace referencia y creará una entrada debajo del texto principal al final de la página.
// Esta entrada contendrá la marca de referencia de la nota al pie y el texto de referencia,
// que pasaremos al método "InsertFootnote" del generador de documentos.
builder->Write(u"Main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// Si esta propiedad se establece en "true", entonces la marca de referencia de nuestra nota al pie
// será su índice entre todas las notas al pie de la sección.
// Esta es la primera nota al pie, por lo que la marca de referencia será "1".
ASSERT_TRUE(footnote->get_IsAuto());

// Podemos mover el generador de documentos dentro de la nota al pie para editar su texto de referencia.
builder->MoveTo(footnote->get_FirstParagraph());
builder->Write(u" More text added by a DocumentBuilder.");
builder->MoveToDocumentEnd();

ASSERT_EQ(u"\u0002 Footnote text. More text added by a DocumentBuilder.", footnote->GetText().Trim());

builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// Podemos establecer una marca de referencia personalizada que la nota al pie usará en lugar de su número de índice.
footnote->set_ReferenceMark(u"RefMark");

ASSERT_FALSE(footnote->get_IsAuto());

// Un marcador con la bandera "IsAuto" establecida en true aún mostrará su índice real
// incluso si los marcadores anteriores muestran marcas de referencia personalizadas, por lo que la marca de referencia de este marcador será "3".
builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

ASSERT_TRUE(footnote->get_IsAuto());

doc->Save(get_ArtifactsDir() + u"InlineStory.AddFootnote.docx");
```

## Ver también

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
