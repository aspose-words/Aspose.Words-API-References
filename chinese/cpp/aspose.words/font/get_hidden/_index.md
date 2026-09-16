---
title: "Aspose::Words::Font::get_Hidden 方法"
linktitle: "get_Hidden"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_Hidden 方法。如果字体在 C++ 中被设置为隐藏文本，则返回 true。"
type: docs
weight: 16000
url: /zh/cpp/aspose.words/font/get_hidden/
---
## Font::get_Hidden method


如果字体被格式化为隐藏文本，则为 True。

```cpp
bool Aspose::Words::Font::get_Hidden()
```


## 示例



展示如何创建一段隐藏文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 当 Hidden 标志设置为 true 时，使用此 Font 对象创建的任何文本在文档中将不可见。
// 除非我们启用 "Hidden text" 选项，否则我们将看不到或无法高亮隐藏文本
// 可在 Microsoft Word 的 "File" -> "Options" -> "Display" 中找到。文本仍然存在，
// 并且我们可以通过编程方式访问这些文本。
// 不建议使用此方法来隐藏敏感信息。
builder->get_Font()->set_Hidden(true);
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text will not be visible in the document.");

doc->Save(get_ArtifactsDir() + u"Font.Hidden.docx");
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
