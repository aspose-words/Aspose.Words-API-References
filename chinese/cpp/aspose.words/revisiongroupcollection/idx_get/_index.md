---
title: "Aspose::Words::RevisionGroupCollection::idx_get 方法"
linktitle: "idx_get"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::RevisionGroupCollection::idx_get 方法。返回指定索引处的修订组（C++）。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words/revisiongroupcollection/idx_get/
---
## RevisionGroupCollection::idx_get method


返回指定索引处的修订组。

```cpp
System::SharedPtr<Aspose::Words::RevisionGroup> Aspose::Words::RevisionGroupCollection::idx_get(int32_t index)
```


## 示例



展示如何在文档中获取一组修订。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

System::SharedPtr<Aspose::Words::RevisionGroup> revisionGroup = doc->get_Revisions()->get_Groups()->idx_get(0);
```

## 另见

* Class [RevisionGroup](../../revisiongroup/)
* Class [RevisionGroupCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
