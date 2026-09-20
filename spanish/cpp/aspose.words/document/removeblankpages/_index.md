---
title: "Método Aspose::Words::Document::RemoveBlankPages"
linktitle: "RemoveBlankPages"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Document::RemoveBlankPages. Elimina páginas en blanco del documento en C++."
type: docs
weight: 67500
url: /es/cpp/aspose.words/document/removeblankpages/
---
## Document::RemoveBlankPages method


Elimina páginas en blanco del documento.

```cpp
System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::Document::RemoveBlankPages()
```


### ReturnValue

La lista de números de página se ha considerado en blanco y se ha eliminado.

## Ejemplos



Muestra cómo eliminar páginas en blanco del documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Blank pages.docx");
ASSERT_EQ(2, doc->get_PageCount());
doc->RemoveBlankPages();
doc->UpdatePageLayout();
ASSERT_EQ(1, doc->get_PageCount());
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
