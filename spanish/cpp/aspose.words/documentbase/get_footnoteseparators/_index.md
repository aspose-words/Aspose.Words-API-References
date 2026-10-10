---
title: "Aspose::Words::DocumentBase::get_FootnoteSeparators método"
linktitle: "get_FootnoteSeparators"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBase::get_FootnoteSeparators método. Proporciona acceso a los separadores de notas al pie/nota al final definidos en el documento en C++."
type: docs
weight: 4500
url: /es/cpp/aspose.words/documentbase/get_footnoteseparators/
---
## DocumentBase::get_FootnoteSeparators method


Proporciona acceso a los separadores de notas al pie/nota final definidos en el documento.

```cpp
System::SharedPtr<Aspose::Words::Notes::FootnoteSeparatorCollection> Aspose::Words::DocumentBase::get_FootnoteSeparators() const
```


## Ejemplos



Muestra cómo eliminar el separador de nota final.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> endnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::EndnoteSeparator);
// Eliminar separador de nota final.
endnoteSeparator->get_FirstParagraph()->get_FirstChild()->Remove();
```


Muestra cómo administrar el formato del separador de notas al pie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> footnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::FootnoteSeparator);
// Alinear el separador de notas al pie.
footnoteSeparator->get_FirstParagraph()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
```

## Ver también

* Class [FootnoteSeparatorCollection](../../../aspose.words.notes/footnoteseparatorcollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
