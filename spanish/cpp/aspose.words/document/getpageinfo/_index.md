---
title: "Aspose::Words::Document::GetPageInfo método"
linktitle: "GetPageInfo"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::GetPageInfo método. Obtiene el tamaño de página, la orientación y otra información sobre una página que podría ser útil para imprimir o renderizar en C++."
type: docs
weight: 62000
url: /es/cpp/aspose.words/document/getpageinfo/
---
## Document::GetPageInfo method


Obtiene el tamaño de página, la orientación y otra información sobre una página que podría ser útil para imprimir o renderizar.

```cpp
System::SharedPtr<Aspose::Words::Rendering::PageInfo> Aspose::Words::Document::GetPageInfo(int32_t pageIndex)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pageIndex | int32_t | El índice de página basado en cero. |

## Ejemplos



Muestra cómo comprobar si la página está en color o no.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Verifique que la primera página del documento no esté coloreada.
ASSERT_FALSE(doc->GetPageInfo(0)->get_Colored());
```

## Ver también

* Class [PageInfo](../../../aspose.words.rendering/pageinfo/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
