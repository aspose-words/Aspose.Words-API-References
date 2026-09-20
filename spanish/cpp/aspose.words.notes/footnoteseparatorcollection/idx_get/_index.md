---
title: "Método idx_get de Aspose::Words::Notes::FootnoteSeparatorCollection"
linktitle: "idx_get"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método idx_get de Aspose::Words::Notes::FootnoteSeparatorCollection. Recupera un FootnoteSeparator del tipo especificado en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.notes/footnoteseparatorcollection/idx_get/
---
## FootnoteSeparatorCollection::idx_get method


Recupera un [FootnoteSeparator](../../footnoteseparator/) del tipo especificado.

```cpp
System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> Aspose::Words::Notes::FootnoteSeparatorCollection::idx_get(Aspose::Words::Notes::FootnoteSeparatorType separatorType)
```


## Ejemplos



Muestra cómo administrar el formato del separador de notas al pie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> footnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::FootnoteSeparator);
// Alinear el separador de notas al pie.
footnoteSeparator->get_FirstParagraph()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
```

## Ver también

* Class [FootnoteSeparator](../../footnoteseparator/)
* Enum [FootnoteSeparatorType](../../footnoteseparatortype/)
* Class [FootnoteSeparatorCollection](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
