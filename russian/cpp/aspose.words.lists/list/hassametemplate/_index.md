---
title: "Aspose::Words::Lists::List::HasSameTemplate метод"
linktitle: "HasSameTemplate"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Lists::List::HasSameTemplate метод. Возвращает true, если текущий список и указанный список созданы из одного и того же шаблона в C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words.lists/list/hassametemplate/
---
## List::HasSameTemplate method


Возвращает true, если текущий список и указанный список созданы из одного шаблона.

```cpp
bool Aspose::Words::Lists::List::HasSameTemplate(const System::SharedPtr<Aspose::Words::Lists::List> &other)
```


## Примеры



Показывает, как определить списки с одинаковым ListDefId.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Different lists.docx");

ASSERT_TRUE(doc->get_Lists()->idx_get(0)->HasSameTemplate(doc->get_Lists()->idx_get(1)));
ASSERT_FALSE(doc->get_Lists()->idx_get(1)->HasSameTemplate(doc->get_Lists()->idx_get(2)));
```

## См. также

* Class [List](../)
* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
