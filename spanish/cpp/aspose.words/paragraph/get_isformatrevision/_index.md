---
title: "Método Aspose::Words::Paragraph::get_IsFormatRevision"
linktitle: "get_IsFormatRevision"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Paragraph::get_IsFormatRevision. Devuelve true si el formato del objeto se cambió en Microsoft Word mientras el seguimiento de cambios estaba habilitado en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words/paragraph/get_isformatrevision/
---
## Paragraph::get_IsFormatRevision method


Devuelve true si el formato del objeto se modificó en Microsoft Word mientras el seguimiento de cambios estaba habilitado.

```cpp
bool Aspose::Words::Paragraph::get_IsFormatRevision()
```


## Ejemplos



Muestra cómo comprobar si un párrafo es una revisión de formato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Format revision.docx");

// Este párrafo es una revisión de "Formato", que ocurre cuando cambiamos el formato del texto existente
// mientras se rastrean revisiones en Microsoft Word mediante \"Review\" -> \"Track changes\".
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_IsFormatRevision());
```

## Ver también

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
