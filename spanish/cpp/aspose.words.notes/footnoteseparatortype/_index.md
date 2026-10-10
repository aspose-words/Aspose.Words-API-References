---
title: "Aspose::Words::Notes::FootnoteSeparatorType enum"
linktitle: "FootnoteSeparatorType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Notes::FootnoteSeparatorType enum. Especifica el tipo del separador de nota al pie/nota final en C++."
type: docs
weight: 6500
url: /es/cpp/aspose.words.notes/footnoteseparatortype/
---
## FootnoteSeparatorType enum


Especifica el tipo del separador de nota al pie/nota final.

```cpp
enum class FootnoteSeparatorType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| FootnoteSeparator | 0 | Separador entre el texto principal y el texto de la nota al pie. |
| FootnoteContinuationSeparator | 1 | Impreso encima del texto de la nota al pie en una página cuando el texto debe continuarse desde una página anterior. |
| FootnoteContinuationNotice | 2 | Impreso debajo del texto de la nota al pie en una página cuando el texto de la nota al pie debe continuarse en una página siguiente. |
| EndnoteSeparator | 3 | Separador entre el texto principal y el texto de la nota final. |
| EndnoteContinuationSeparator | 4 | Impreso encima del texto de la nota final en una página cuando el texto debe continuarse desde una página anterior. |
| EndnoteContinuationNotice | 5 | Impreso debajo del texto de la nota final en una página cuando el texto de la nota final debe continuarse en una página siguiente. |


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

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
