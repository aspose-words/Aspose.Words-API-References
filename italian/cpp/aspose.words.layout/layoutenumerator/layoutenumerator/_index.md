---
title: "Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator costruttore"
linktitle: "LayoutEnumerator"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator costruttore. Inizializza una nuova istanza di questa classe in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.layout/layoutenumerator/layoutenumerator/
---
## LayoutEnumerator::LayoutEnumerator constructor


Inizializza una nuova istanza di questa classe.

```cpp
Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator(const System::SharedPtr<Aspose::Words::Document> &document)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| documento | const System::SharedPtr\<Aspose::Words::Document\>\& | Un documento il cui modello di layout di pagina deve essere enumerato. |
## Note


Se il modello di layout di pagina del documento non è stato costruito, l'enumeratore chiama [UpdatePageLayout](../../../aspose.words/document/updatepagelayout/) per costruirlo.

Ogni volta che il documento viene aggiornato e viene creato un nuovo modello di layout di pagina, è necessario utilizzare un nuovo enumeratore per accedervi.

## Vedi anche

* Class [Document](../../../aspose.words/document/)
* Class [LayoutEnumerator](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
