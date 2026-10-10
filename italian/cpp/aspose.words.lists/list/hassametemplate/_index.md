---
title: "Aspose::Words::Lists::List::HasSameTemplate metodo"
linktitle: "HasSameTemplate"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Lists::List::HasSameTemplate metodo. Restituisce true se l'elenco corrente e l'elenco fornito sono creati dallo stesso modello in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words.lists/list/hassametemplate/
---
## List::HasSameTemplate method


Restituisce true se l'elenco corrente e l'elenco fornito sono creati dallo stesso modello.

```cpp
bool Aspose::Words::Lists::List::HasSameTemplate(const System::SharedPtr<Aspose::Words::Lists::List> &other)
```


## Esempi



Mostra come definire elenchi con lo stesso ListDefId.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Different lists.docx");

ASSERT_TRUE(doc->get_Lists()->idx_get(0)->HasSameTemplate(doc->get_Lists()->idx_get(1)));
ASSERT_FALSE(doc->get_Lists()->idx_get(1)->HasSameTemplate(doc->get_Lists()->idx_get(2)));
```

## Vedi anche

* Class [List](../)
* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
