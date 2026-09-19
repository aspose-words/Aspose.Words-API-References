---
title: "Aspose::Words::Markup::SmartTag::SmartTag costruttore"
linktitle: "SmartTag"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::SmartTag::SmartTag costruttore. Inizializza una nuova istanza della classe SmartTag in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.markup/smarttag/smarttag/
---
## SmartTag::SmartTag constructor


Inizializza una nuova istanza della classe [SmartTag](../).

```cpp
Aspose::Words::Markup::SmartTag::SmartTag(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Il documento proprietario. |
## Note


Quando crei un nuovo nodo, devi specificare un documento a cui il nodo appartiene. Un nodo non può esistere senza un documento perché dipende dalle strutture a livello di documento, come elenchi e stili. Sebbene un nodo appartenga sempre a un documento, un nodo può o non può far parte dell'albero del documento.

Quando un nodo viene creato, appartiene a un documento, ma non è ancora parte dell'albero del documento e [ParentNode](../../../aspose.words/node/get_parentnode/) è nullo. Per inserire un nodo nel documento, utilizza i metodi [InsertAfter1()</see> o <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) sul nodo genitore.

## Vedi anche

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [SmartTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
