---
title: "Aspose::Words::DocumentBuilder::MoveToSection 方法"
linktitle: "MoveToSection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::MoveToSection 方法。将光标移动到指定章节中正文的开头（C++）。"
type: docs
weight: 60000
url: /zh/cpp/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder::MoveToSection method


将光标移动到指定节正文的开头。

```cpp
void Aspose::Words::DocumentBuilder::MoveToSection(int32_t sectionIndex)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| sectionIndex | int32_t | 要移动到的章节索引。 |
## 备注


当 *sectionIndex* 大于或等于 0 时，它表示从文档开头算起的索引，0 表示第一章节。 当 *sectionIndex* 小于 0 时，它表示从文档末尾算起的索引，-1 表示最后一章节。

光标被移动到指定章节的 [Body](../../body/) 中的第一段落。

## 另见

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
