---
title: "Aspose::Words::Notes::FootnoteOptions::get_NumberStyle método"
linktitle: "get_NumberStyle"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Notes::FootnoteOptions::get_NumberStyle método. Especifica el formato numérico para notas al pie numeradas automáticamente en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.notes/footnoteoptions/get_numberstyle/
---
## FootnoteOptions::get_NumberStyle method


Especifica el formato numérico para notas al pie numeradas automáticamente.

```cpp
Aspose::Words::NumberStyle Aspose::Words::Notes::FootnoteOptions::get_NumberStyle() override
```

## Observaciones


No todos los estilos de número son aplicables a esta propiedad. Para la lista de estilos de número aplicables, consulte el cuadro de diálogo Insertar [Footnote](../../footnote/) o Endnote en Microsoft Word. Si selecciona un estilo de número que no es aplicable, Microsoft Word volverá al valor predeterminado.

## Ejemplos



Muestra cómo cambiar el estilo de numeración de los símbolos de referencia de notas al pie/notas finales.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Las notas al pie y las notas finales son una forma de adjuntar una referencia o un comentario al texto.
// que no interfiere con el flujo del texto principal.
// Insertar una nota al pie/notas finales agrega un pequeño símbolo de referencia en superíndice.
// en el texto principal donde insertamos la nota al pie/notas finales.
// Cada nota al pie/notas finales también crea una entrada, que consiste en un símbolo que coincide con la referencia
// del símbolo en el texto principal. El texto de referencia que pasamos al método "InsertEndnote" del generador de documentos.
// Las entradas de notas al pie, por defecto, aparecen al final de cada página que contiene
// sus símbolos de referencia, y las notas finales aparecen al final del documento.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.", u"Custom footnote reference mark");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.", u"Custom endnote reference mark");

// Por defecto, el símbolo de referencia de cada nota al pie y nota final es su índice
// entre todas las notas al pie/notas finales del documento. Cada documento mantiene recuentos separados
// para notas al pie y para notas finales. Por defecto, las notas al pie muestran sus números usando numerales arábigos,
// y las notas finales muestran sus números en numerales romanos en minúscula.
ASSERT_EQ(Aspose::Words::NumberStyle::Arabic, doc->get_FootnoteOptions()->get_NumberStyle());
ASSERT_EQ(Aspose::Words::NumberStyle::LowercaseRoman, doc->get_EndnoteOptions()->get_NumberStyle());

// Podemos usar la propiedad "NumberStyle" para aplicar estilos de numeración personalizados a notas al pie y notas finales.
// Esto no afectará a las notas al pie/notas finales con marcas de referencia personalizadas.
doc->get_FootnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
doc->get_EndnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseLetter);

doc->Save(get_ArtifactsDir() + u"InlineStory.RefMarkNumberStyle.docx");
```

## Ver también

* Enum [NumberStyle](../../../aspose.words/numberstyle/)
* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
