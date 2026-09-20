---
title: "Método Aspose::Words::NodeCollection::Insert"
linktitle: "Insert"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::NodeCollection::Insert. Inserta un nodo en la colección en el índice especificado en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words/nodecollection/insert/
---
## NodeCollection::Insert method


Inserta un nodo en la colección en el índice especificado.

```cpp
void Aspose::Words::NodeCollection::Insert(int32_t index, const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| index | int32_t | El índice basado en cero del nodo. Se permiten índices negativos y indican acceso desde el final de la lista. Por ejemplo, -1 significa el último nodo, -2 el penúltimo y así sucesivamente. |
| nodo | const System::SharedPtr\<Aspose::Words::Node\>\& | El nodo a insertar. |
## Observaciones


El nodo se inserta como hijo en el objeto nodo del cual se creó la colección.

Si el índice es igual o mayor que [Count](../get_count/), el nodo se agrega al final de la colección.

Si el índice es negativo y su valor absoluto es mayor que [Count](../get_count/), el nodo se agrega al final de la colección.

Si el nodo que se está insertando fue creado a partir de otro documento, debe usar [ImportNode()](../) para importar el nodo al documento actual. El nodo importado puede entonces insertarse en el documento actual.

## Ejemplos



Muestra cómo trabajar con una [NodeCollection](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Agrega texto al documento insertando Runs usando un DocumentBuilder.
builder->Write(u"Run 1. ");
builder->Write(u"Run 2. ");

// Cada invocación del método "Write" crea un nuevo Run,
// que luego aparece en la RunCollection del párrafo padre.
System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();

ASSERT_EQ(2, runs->get_Count());

// También podemos insertar un nodo en la RunCollection manualmente.
auto newRun = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");
runs->Insert(3, newRun);

ASSERT_TRUE(runs->Contains(newRun));
ASSERT_EQ(u"Run 1. Run 2. Run 3.", doc->GetText().Trim());

// Accede a los runs individuales y elimínalos para quitar su texto del documento.
System::SharedPtr<Aspose::Words::Run> run = runs->idx_get(1);
runs->Remove(run);

ASSERT_EQ(u"Run 1. Run 3.", doc->GetText().Trim());
ASSERT_FALSE(System::TestTools::IsNull(run));
ASSERT_FALSE(runs->Contains(run));
```

## Ver también

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
