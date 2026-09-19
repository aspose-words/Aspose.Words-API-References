---
title: "Aspose::Words::NodeList::ToArray method"
linktitle: "ToArray"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::NodeList::ToArray method. Copia tutti i nodi dalla collezione in un nuovo array di nodi in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words/nodelist/toarray/
---
## NodeList::ToArray method


Copia tutti i nodi dalla raccolta in un nuovo array di nodi.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Node>> Aspose::Words::NodeList::ToArray() const
```


### ReturnValue

Un array di nodi.
## Note


Non dovresti aggiungere/rimuovere nodi mentre iteri su una collezione di nodi perché invalida l'iteratore e richiede aggiornamenti per le collezioni live.

Per poter aggiungere/rimuovere nodi durante l'iterazione, usa questo metodo per copiare i nodi in un array a dimensione fissa e poi iterare sull'array.

## Vedi anche

* Class [Node](../../node/)
* Class [NodeList](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
