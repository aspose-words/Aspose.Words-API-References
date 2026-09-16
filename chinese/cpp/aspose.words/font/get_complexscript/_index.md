---
title: "Aspose::Words::Font::get_ComplexScript 方法"
linktitle: "get_ComplexScript"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_ComplexScript 方法。指定在 C++ 中确定此运行的格式时，无论其 Unicode 字符值如何，都应将此运行的内容视为复杂脚本文本。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words/font/get_complexscript/
---
## Font::get_ComplexScript method


指定在确定此运行的格式时，无论其 Unicode 字符值如何，是否应将此运行的内容视为复杂脚本文本。

```cpp
bool Aspose::Words::Font::get_ComplexScript()
```


## 示例



展示如何添加始终被视为复杂脚本的文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_ComplexScript(true);

builder->Writeln(u"Text treated as complex script.");

doc->Save(get_ArtifactsDir() + u"Font.ComplexScript.docx");
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
