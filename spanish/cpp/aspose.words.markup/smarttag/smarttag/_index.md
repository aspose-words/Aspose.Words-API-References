---
title: "Constructor Aspose::Words::Markup::SmartTag::SmartTag"
linktitle: "SmartTag"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Constructor Aspose::Words::Markup::SmartTag::SmartTag. Inicializa una nueva instancia de la clase SmartTag en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.markup/smarttag/smarttag/
---
## SmartTag::SmartTag constructor


Inicializa una nueva instancia de la clase [SmartTag](../).

```cpp
Aspose::Words::Markup::SmartTag::SmartTag(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | El documento propietario. |
## Observaciones


Cuando crea un nuevo nodo, debe especificar un documento al que pertenece el nodo. Un nodo no puede existir sin un documento porque depende de las estructuras del documento, como listas y estilos. Aunque un nodo siempre pertenece a un documento, puede o no ser parte del árbol del documento.

Cuando se crea un nodo, pertenece a un documento, pero aún no forma parte del árbol del documento y [ParentNode](../../../aspose.words/node/get_parentnode/) es nulo. Para insertar un nodo en el documento, use los métodos [InsertAfter1()</see> o <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) en el nodo padre.

## Ver también

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [SmartTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
