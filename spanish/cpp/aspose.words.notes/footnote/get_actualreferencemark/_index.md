---
title: "Aspose::Words::Notes::Footnote::get_ActualReferenceMark método"
linktitle: "get_ActualReferenceMark"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Notes::Footnote::get_ActualReferenceMark método. Obtiene el texto real de la marca de referencia que se muestra en el documento para esta nota al pie en C++."
type: docs
weight: 3834
url: /es/cpp/aspose.words.notes/footnote/get_actualreferencemark/
---
## Footnote::get_ActualReferenceMark method


Obtiene el texto real de la marca de referencia mostrada en el documento para esta nota al pie.

```cpp
System::String Aspose::Words::Notes::Footnote::get_ActualReferenceMark()
```


## Ejemplos



Muestra cómo obtener la marca de referencia real de la nota al pie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

auto footnote = System::ExplicitCast<Aspose::Words::Notes::Footnote>(doc->GetChild(Aspose::Words::NodeType::Footnote, 1, true));
doc->UpdateFields();
doc->UpdateActualReferenceMarks();

ASSERT_EQ(u"1", footnote->get_ActualReferenceMark());
```

## Ver también

* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
