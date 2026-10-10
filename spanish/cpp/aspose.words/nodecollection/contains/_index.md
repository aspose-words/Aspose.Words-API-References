---
title: "Aspose::Words::NodeCollection::Contains método"
linktitle: "Contains"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::NodeCollection::Contains método. Determina si un nodo está en la colección en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/nodecollection/contains/
---
## NodeCollection::Contains method


Determina si un nodo está en la colección.

```cpp
bool Aspose::Words::NodeCollection::Contains(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nodo | const System::SharedPtr\<Aspose::Words::Node\>\& | El nodo a localizar. |

### ReturnValue

**true** if item is found in the collection; otherwise, **false**.
## Observaciones


Este método realiza una búsqueda lineal; por lo tanto, el tiempo medio de ejecución es proporcional a [Count](../get_count/).

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
