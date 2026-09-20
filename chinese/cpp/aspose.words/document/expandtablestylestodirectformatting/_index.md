---
title: "Aspose::Words::Document::ExpandTableStylesToDirectFormatting 方法"
linktitle: "ExpandTableStylesToDirectFormatting"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::ExpandTableStylesToDirectFormatting 方法。将表格样式中指定的格式转换为文档中表格的直接格式（C++）。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words/document/expandtablestylestodirectformatting/
---
## Document::ExpandTableStylesToDirectFormatting method


将表格样式中指定的格式转换为文档中表格的直接格式。

```cpp
void Aspose::Words::Document::ExpandTableStylesToDirectFormatting()
```

## 备注


此方法的存在是因为此版本的 Aspose.Words 对表格样式的支持仅限（见下文）。当您加载包含使用表格样式格式化的表格的 DOCX 或 WordprocessingML 文档，并且需要查询表格、单元格、段落或文本的格式时，此方法可能会很有用。

此版本的 Aspose.Words 对表格样式的有限支持如下：

* Table styles defined in DOCX or WordprocessingML documents are preserved as table styles when saving the document as DOCX or WordprocessingML.
* Table styles defined in DOCX or WordprocessingML documents are automatically converted to direct formatting on tables when saving the document into any other format, rendering or printing.
* Table styles defined in DOC documents are preserved as table styles when saving the document as DOC only.


## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
