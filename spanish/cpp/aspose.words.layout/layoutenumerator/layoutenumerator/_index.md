---
title: "Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator constructor"
linktitle: "LayoutEnumerator"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator constructor. Inicializa una nueva instancia de esta clase en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.layout/layoutenumerator/layoutenumerator/
---
## LayoutEnumerator::LayoutEnumerator constructor


Inicializa una nueva instancia de esta clase.

```cpp
Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator(const System::SharedPtr<Aspose::Words::Document> &document)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| documento | const System::SharedPtr\<Aspose::Words::Document\>\& | Un documento cuyo modelo de diseño de página se va a enumerar. |
## Observaciones


Si el modelo de diseño de página del documento no ha sido construido, el enumerador llama a [UpdatePageLayout](../../../aspose.words/document/updatepagelayout/) para construirlo.

Cada vez que el documento se actualiza y se crea un nuevo modelo de diseño de página, se debe usar un nuevo enumerador para acceder a él.

## Ver también

* Class [Document](../../../aspose.words/document/)
* Class [LayoutEnumerator](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
