---
title: "Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator 构造函数"
linktitle: "LayoutEnumerator"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator 构造函数。初始化此类在 C++ 中的新实例。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.layout/layoutenumerator/layoutenumerator/
---
## LayoutEnumerator::LayoutEnumerator constructor


初始化此类的新实例。

```cpp
Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator(const System::SharedPtr<Aspose::Words::Document> &document)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文档 | const System::SharedPtr\<Aspose::Words::Document\>\& | 要枚举其页面布局模型的文档。 |
## 备注


如果文档的页面布局模型尚未构建，枚举器将调用 [UpdatePageLayout](../../../aspose.words/document/updatepagelayout/) 来构建它。

每当文档更新并创建新的页面布局模型时，必须使用新的枚举器来访问它。

## 另见

* Class [Document](../../../aspose.words/document/)
* Class [LayoutEnumerator](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
