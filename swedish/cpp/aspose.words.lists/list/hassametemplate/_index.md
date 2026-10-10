---
title: "Aspose::Words::Lists::List::HasSameTemplate metod"
linktitle: "HasSameTemplate"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Lists::List::HasSameTemplate metod. Returnerar true om den aktuella listan och den angivna listan är skapade från samma mall i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words.lists/list/hassametemplate/
---
## List::HasSameTemplate method


Returnerar true om den aktuella listan och den angivna listan är skapade från samma mall.

```cpp
bool Aspose::Words::Lists::List::HasSameTemplate(const System::SharedPtr<Aspose::Words::Lists::List> &other)
```


## Exempel



Visar hur man definierar listor med samma ListDefId.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Different lists.docx");

ASSERT_TRUE(doc->get_Lists()->idx_get(0)->HasSameTemplate(doc->get_Lists()->idx_get(1)));
ASSERT_FALSE(doc->get_Lists()->idx_get(1)->HasSameTemplate(doc->get_Lists()->idx_get(2)));
```

## Se även

* Class [List](../)
* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
