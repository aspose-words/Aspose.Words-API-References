---
title: "Aspose::Words::Lists::List::HasSameTemplate método"
linktitle: "HasSameTemplate"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Lists::List::HasSameTemplate método. Devuelve true si la lista actual y la lista dada se crean a partir de la misma plantilla en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words.lists/list/hassametemplate/
---
## List::HasSameTemplate method


Devuelve true si la lista actual y la lista dada se crean a partir de la misma plantilla.

```cpp
bool Aspose::Words::Lists::List::HasSameTemplate(const System::SharedPtr<Aspose::Words::Lists::List> &other)
```


## Ejemplos



Muestra cómo definir listas con el mismo ListDefId.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Different lists.docx");

ASSERT_TRUE(doc->get_Lists()->idx_get(0)->HasSameTemplate(doc->get_Lists()->idx_get(1)));
ASSERT_FALSE(doc->get_Lists()->idx_get(1)->HasSameTemplate(doc->get_Lists()->idx_get(2)));
```

## Ver también

* Class [List](../)
* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
