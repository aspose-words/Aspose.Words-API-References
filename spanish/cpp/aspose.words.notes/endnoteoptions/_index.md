---
title: "Clase Aspose::Words::Notes::EndnoteOptions"
linktitle: "EndnoteOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Notes::EndnoteOptions. Representa las opciones de numeración de notas finales para un documento o sección. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.notes/endnoteoptions/
---
## EndnoteOptions class


Representa las opciones de numeración de notas al final para un documento o sección. Para obtener más información, visite el artículo de documentación [Working with Footnote and Endnote](https://docs.aspose.com/words/cpp/working-with-footnote-and-endnote/).

```cpp
class EndnoteOptions : public Aspose::Words::Notes::IFootnoteOptions
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_NumberStyle](./get_numberstyle/)() override | Especifica el formato numérico para notas finales numeradas automáticamente. |
| [get_Position](./get_position/)() | Especifica la posición de las notas finales. |
| [get_RestartRule](./get_restartrule/)() override | Determina cuándo se reinicia la numeración automática. |
| [get_StartNumber](./get_startnumber/)() override | Especifica el número o carácter inicial para la primera nota final numerada automáticamente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_NumberStyle](./set_numberstyle/)(Aspose::Words::NumberStyle) override | Establecedor para [Aspose::Words::Notes::EndnoteOptions::get_NumberStyle](./get_numberstyle/). |
| [set_Position](./set_position/)(Aspose::Words::Notes::EndnotePosition) | Establecedor para [Aspose::Words::Notes::EndnoteOptions::get_Position](./get_position/). |
| [set_RestartRule](./set_restartrule/)(Aspose::Words::Notes::FootnoteNumberingRule) override | Establecedor para [Aspose::Words::Notes::EndnoteOptions::get_RestartRule](./get_restartrule/). |
| [set_StartNumber](./set_startnumber/)(int32_t) override | Establecedor para [Aspose::Words::Notes::EndnoteOptions::get_StartNumber](./get_startnumber/). |
| static [Type](./type/)() |  |

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


Muestra cómo reiniciar la numeración de notas al pie/notas finales en ciertos lugares del documento.
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
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.");
builder->Write(u"Text 4. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 4.");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.");
builder->Write(u"Text 4. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 4.");

// Por defecto, el símbolo de referencia de cada nota al pie y nota final es su índice
// entre todas las notas al pie/notas finales del documento. Cada documento mantiene recuentos separados
// para notas al pie y notas finales y no reinicia estos recuentos en ningún momento.
ASSERT_EQ(doc->get_FootnoteOptions()->get_RestartRule(), Aspose::Words::Notes::FootnoteNumberingRule::Default);
ASSERT_EQ(Aspose::Words::Notes::FootnoteNumberingRule::Default, Aspose::Words::Notes::FootnoteNumberingRule::Continuous);

// Podemos usar la propiedad "RestartRule" para que el documento reinicie
// los recuentos de notas al pie/notas finales en una nueva página o sección.
doc->get_FootnoteOptions()->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartPage);
doc->get_EndnoteOptions()->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartSection);

doc->Save(get_ArtifactsDir() + u"InlineStory.NumberingRule.docx");
```


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

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
