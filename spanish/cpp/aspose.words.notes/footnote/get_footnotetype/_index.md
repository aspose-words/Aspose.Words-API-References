---
title: "Aspose::Words::Notes::Footnote::get_FootnoteType método"
linktitle: "get_FootnoteType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Notes::Footnote::get_FootnoteType método. Devuelve un valor que especifica si se trata de una nota al pie o una nota al final en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.notes/footnote/get_footnotetype/
---
## Footnote::get_FootnoteType method


Devuelve un valor que especifica si esto es una nota al pie o una nota final.

```cpp
Aspose::Words::Notes::FootnoteType Aspose::Words::Notes::Footnote::get_FootnoteType() const
```


## Ejemplos



Muestra la diferencia entre notas al pie y notas al final.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A continuación se presentan dos formas de adjuntar referencias numeradas al texto. Ambas referencias agregarán un
// pequeño signo de referencia en superíndice en la ubicación donde los insertamos.
// El signo de referencia, por defecto, es el número de índice de la referencia entre todas las referencias del documento.
// Cada referencia también creará una entrada, que tendrá el mismo signo de referencia que en el texto principal
// y texto de referencia, que pasaremos al método \"InsertFootnote\" del generador de documentos.
// 1 -  Una nota al pie, cuya entrada aparecerá en la misma página que el texto al que hace referencia:
builder->Write(u"Footnote referenced main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 -  Una nota al final, cuya entrada aparecerá al final del documento:
builder->Write(u"Endnote referenced main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> endnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote text, will appear at the very end of the document.");

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Notes::FootnoteType::Footnote, footnote->get_FootnoteType());
ASSERT_EQ(Aspose::Words::Notes::FootnoteType::Endnote, endnote->get_FootnoteType());

doc->Save(get_ArtifactsDir() + u"InlineStory.FootnoteEndnote.docx");
```

## Ver también

* Enum [FootnoteType](../../footnotetype/)
* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
