---
title: "Aspose::Words::Notes::Footnote::get_IsAuto method"
linktitle: "get_IsAuto"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Notes::Footnote::get_IsAuto method. Contiene un valor que especifica si se trata de una nota al pie autogenerada o una nota al pie con una marca de referencia personalizada definida por el usuario en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.notes/footnote/get_isauto/
---
## Footnote::get_IsAuto method


Contiene un valor que especifica si esta es una nota al pie autogenerada o una nota al pie con una marca de referencia personalizada definida por el usuario.

```cpp
bool Aspose::Words::Notes::Footnote::get_IsAuto() const
```


## Ejemplos



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

* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
