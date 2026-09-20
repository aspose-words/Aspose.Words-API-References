---
title: "Método get_Columns de Aspose::Words::Notes::FootnoteOptions"
linktitle: "get_Columns"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método get_Columns de Aspose::Words::Notes::FootnoteOptions. Especifica el número de columnas con las que se formatea el área de notas al pie en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.notes/footnoteoptions/get_columns/
---
## FootnoteOptions::get_Columns method


Especifica el número de columnas con las que se formatea el área de notas al pie.

```cpp
int32_t Aspose::Words::Notes::FootnoteOptions::get_Columns()
```


## Ejemplos



Muestra cómo dividir la sección de notas al pie en un número determinado de columnas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

doc->get_FootnoteOptions()->set_Columns(2);
doc->Save(get_ArtifactsDir() + u"Document.FootnoteColumns.docx");
```

## Ver también

* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
