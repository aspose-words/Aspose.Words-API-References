---
title: "Aspose::Words::Notes::FootnoteOptions::get_StartNumber método"
linktitle: "get_StartNumber"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Notes::FootnoteOptions::get_StartNumber método. Especifica el número o carácter inicial para la primera nota al pie numerada automáticamente en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.notes/footnoteoptions/get_startnumber/
---
## FootnoteOptions::get_StartNumber method


Especifica el número o carácter inicial para la primera nota al pie numerada automáticamente.

```cpp
int32_t Aspose::Words::Notes::FootnoteOptions::get_StartNumber() override
```

## Observaciones


Esta propiedad tiene efecto solo cuando [RestartRule](../get_restartrule/) está configurada a [Continuous](../../footnotenumberingrule/).

## Ejemplos



Muestra cómo establecer un número en el que el documento comienza la numeración de notas al pie/notas finales.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Las notas al pie y las notas finales son una forma de adjuntar una referencia o un comentario al texto.
// que no interfiere con el flujo del texto principal.
// Insertar una nota al pie/notas finales agrega un pequeño símbolo de referencia en superíndice.
// en el texto principal donde insertamos la nota al pie/notas finales.
// Cada nota al pie/nota final también crea una entrada, que consiste en un símbolo
// que coincide con el símbolo de referencia en el texto principal.
// El texto de referencia que pasamos al método "InsertEndnote" del constructor de documentos.
// Las entradas de notas al pie, por defecto, aparecen al final de cada página que contiene
// sus símbolos de referencia, y las notas finales aparecen al final del documento.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.");

// Por defecto, el símbolo de referencia de cada nota al pie y nota final es su índice
// entre todas las notas al pie/notas finales del documento. Cada documento mantiene recuentos separados
// para notas al pie y para notas finales, que ambas comienzan en 1.
ASSERT_EQ(1, doc->get_FootnoteOptions()->get_StartNumber());
ASSERT_EQ(1, doc->get_EndnoteOptions()->get_StartNumber());

// Podemos usar la propiedad "StartNumber" para que el documento
// inicie la numeración de una nota al pie o nota final en un número diferente.
doc->get_EndnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::Arabic);
doc->get_EndnoteOptions()->set_StartNumber(50);

doc->Save(get_ArtifactsDir() + u"InlineStory.StartNumber.docx");
```

## Ver también

* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
