---
title: "Aspose::Words::Document::get_PageCount método"
linktitle: "get_PageCount"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::get_PageCount método. Obtiene el número de páginas del documento calculado por la operación de diseño de página más reciente en C++."
type: docs
weight: 43000
url: /es/cpp/aspose.words/document/get_pagecount/
---
## Document::get_PageCount method


Obtiene el número de páginas del documento según lo calculado por la operación de diseño de página más reciente.

```cpp
int32_t Aspose::Words::Document::get_PageCount()
```


## Ejemplos



Muestra cómo contar el número de páginas del documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 3");

// Verifique el recuento de páginas esperado del documento.
ASSERT_EQ(3, doc->get_PageCount());

// Obtener la propiedad PageCount invocó el diseño de página del documento para calcular el valor.
// Esta operación no necesitará repetirse al renderizar el documento a un formato de guardado de página fija,
// como .pdf. Por lo tanto, puede ahorrar tiempo, especialmente con documentos más complejos.
doc->Save(get_ArtifactsDir() + u"Document.GetPageCount.pdf");
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
