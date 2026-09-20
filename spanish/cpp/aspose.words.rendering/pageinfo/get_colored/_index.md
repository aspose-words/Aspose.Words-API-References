---
title: "Método Aspose::Words::Rendering::PageInfo::get_Colored"
linktitle: "get_Colored"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Rendering::PageInfo::get_Colored. Devuelve true si la página contiene contenido a color en C++."
type: docs
weight: 1500
url: /es/cpp/aspose.words.rendering/pageinfo/get_colored/
---
## PageInfo::get_Colored method


Devuelve **true** si la página contiene contenido coloreado.

```cpp
bool Aspose::Words::Rendering::PageInfo::get_Colored()
```


## Ejemplos



Muestra cómo comprobar si la página está en color o no.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Verifique que la primera página del documento no esté coloreada.
ASSERT_FALSE(doc->GetPageInfo(0)->get_Colored());
```

## Ver también

* Class [PageInfo](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
