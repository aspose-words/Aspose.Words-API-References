---
title: "Aspose::Words::Font::get_Italic 方法"
linktitle: "get_Italic"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_Italic 方法。如果字体在 C++ 中被设置为斜体，则返回 true。"
type: docs
weight: 18000
url: /zh/cpp/aspose.words/font/get_italic/
---
## Font::get_Italic method


如果字体设置为斜体，则为 True。

```cpp
bool Aspose::Words::Font::get_Italic()
```


## 示例



展示如何使用 DocumentBuilder 编写斜体文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_Italic(true);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"Font.Italic.docx");
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
