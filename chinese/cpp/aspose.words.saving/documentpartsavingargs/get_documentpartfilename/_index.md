---
title: "Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName 方法"
linktitle: "get_DocumentPartFileName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName 方法。获取或设置文档部件将在 C++ 中保存的文件名（不含路径）。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.saving/documentpartsavingargs/get_documentpartfilename/
---
## DocumentPartSavingArgs::get_DocumentPartFileName method


获取或设置文档部件将保存到的文件名（不含路径）。

```cpp
System::String Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName() const
```

## 备注


此属性允许您重新定义在导出为 HTML 或 EPUB 时文档部件文件名的生成方式。

当回调被调用时，此属性包含由 Aspose.Words 生成的文件名。您可以更改此属性的值，以将文档部件保存到其他文件。请注意，每个部件的文件名必须是唯一的。

[DocumentPartFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name. If output document file name was not specified, for instance when saving to a stream, this file name is used only for referencing document parts. The same is true when saving to EPUB format.

## 另见

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
