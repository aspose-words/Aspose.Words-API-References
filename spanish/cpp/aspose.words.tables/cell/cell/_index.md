---
title: "Aspose::Words::Tables::Cell::Cell constructor"
linktitle: "Celda"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::Cell::Cell constructor. Inicializa una nueva instancia de la clase Cell en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.tables/cell/cell/
---
## Cell::Cell constructor


Inicializa una nueva instancia de la clase [Cell](../).

```cpp
Aspose::Words::Tables::Cell::Cell(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | El documento propietario. |
## Observaciones


Cuando se crea [Cell](../), pertenece al documento especificado, pero aún no forma parte del documento y [ParentNode](../../../aspose.words/node/get_parentnode/) es **null**.

Para agregar [Cell](../) al documento use [InsertAfter1()</see> o <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../) en la fila donde desea insertar la celda.

## Ver también

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
