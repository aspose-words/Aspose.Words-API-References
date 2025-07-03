---
title: Aspose::Words::Lists::List::HasSameTemplate method
linktitle: HasSameTemplate
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Lists::List::HasSameTemplate method. Returns true if the current list and the given list are created from the same template in C++.'
type: docs
weight: 14000
url: /cpp/aspose.words.lists/list/hassametemplate/
---
## List::HasSameTemplate method


Returns true if the current list and the given list are created from the same template.

```cpp
bool Aspose::Words::Lists::List::HasSameTemplate(const System::SharedPtr<Aspose::Words::Lists::List> &other)
```


## Examples



Shows how to define lists with the same ListDefId. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Different lists.docx");

ASSERT_TRUE(doc->get_Lists()->idx_get(0)->HasSameTemplate(doc->get_Lists()->idx_get(1)));
ASSERT_FALSE(doc->get_Lists()->idx_get(1)->HasSameTemplate(doc->get_Lists()->idx_get(2)));
```

## See Also

* Class [List](../)
* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
