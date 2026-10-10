---
title: "Aspose::Words::Font::get_Kerning 方法"
linktitle: "get_Kerning"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_Kerning 方法。获取或设置在 C++ 中开始字距调整的字体大小。"
type: docs
weight: 20000
url: /zh/cpp/aspose.words/font/get_kerning/
---
## Font::get_Kerning method


获取或设置字距调整开始的字体大小。

```cpp
double Aspose::Words::Font::get_Kerning()
```


## 示例



展示如何指定字距调整开始生效的字体大小。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Arial Black");

// 设置构建器的字体大小，以及字距调整生效的最小尺寸。
// 字体大小低于字距阈值，因此下面的段落将没有字距调整。
builder->get_Font()->set_Size(18);
builder->get_Font()->set_Kerning(24);

builder->Writeln(u"TALLY. (Kerning not applied)");

// 设置字距阈值，使构建器当前的字体大小高于该阈值。
// 从此以后我们添加的任何文本都将应用字距调整。字符之间的空格
// 将被调整，通常会使文本段落看起来更美观一些。
builder->get_Font()->set_Kerning(12);

builder->Writeln(u"TALLY. (Kerning applied)");

doc->Save(get_ArtifactsDir() + u"Font.Kerning.docx");
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
