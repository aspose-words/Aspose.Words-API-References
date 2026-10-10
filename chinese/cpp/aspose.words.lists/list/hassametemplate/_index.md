---
title: "Aspose::Words::Lists::List::HasSameTemplate 方法"
linktitle: "HasSameTemplate"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Lists::List::HasSameTemplate 方法。若当前列表和给定列表是从相同模板创建的，则在 C++ 中返回 true。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words.lists/list/hassametemplate/
---
## List::HasSameTemplate method


如果当前列表和给定列表是基于相同模板创建的，则返回 true。

```cpp
bool Aspose::Words::Lists::List::HasSameTemplate(const System::SharedPtr<Aspose::Words::Lists::List> &other)
```


## 示例



展示如何使用相同的 ListDefId 定义列表。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Different lists.docx");

ASSERT_TRUE(doc->get_Lists()->idx_get(0)->HasSameTemplate(doc->get_Lists()->idx_get(1)));
ASSERT_FALSE(doc->get_Lists()->idx_get(1)->HasSameTemplate(doc->get_Lists()->idx_get(2)));
```

## 另见

* Class [List](../)
* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
