---
title: "Aspose::Words::DocumentBuilder::InsertFootnote método"
linktitle: "InsertFootnote"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::InsertFootnote método. Inserta una nota al pie o una nota al final en el documento en C++."
type: docs
weight: 35000
url: /es/cpp/aspose.words/documentbuilder/insertfootnote/
---
## DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType, const System::String\&) method


Inserta una nota al pie o una nota final en el documento.

```cpp
System::SharedPtr<Aspose::Words::Notes::Footnote> Aspose::Words::DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType footnoteType, const System::String &footnoteText)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| footnoteType | Aspose::Words::Notes::FootnoteType | Especifica si se debe insertar una nota al pie o una nota al final. |
| footnoteText | const System::String\& | Especifica el texto de la nota al pie. |

### ReturnValue

Devuelve un objeto de nota al pie que acaba de crearse.

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

## Ver también

* Class [Footnote](../../../aspose.words.notes/footnote/)
* Enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType, const System::String\&, const System::String\&) method


Inserta una nota al pie o una nota final en el documento.

```cpp
System::SharedPtr<Aspose::Words::Notes::Footnote> Aspose::Words::DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType footnoteType, const System::String &footnoteText, const System::String &referenceMark)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| footnoteType | Aspose::Words::Notes::FootnoteType | Especifica si se debe insertar una nota al pie o una nota al final. |
| footnoteText | const System::String\& | Especifica el texto de la nota al pie. |
| referenceMark | const System::String\& | Especifica la marca de referencia personalizada de la nota al pie. |

### ReturnValue

Devuelve un objeto de nota al pie que acaba de crearse.

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

## Ver también

* Class [Footnote](../../../aspose.words.notes/footnote/)
* Enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
