---
title: "Aspose::Words::Font::get_EmphasisMark 方法"
linktitle: "get_EmphasisMark"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_EmphasisMark 方法。获取或设置应用于此格式的强调标记（C++）。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words/font/get_emphasismark/
---
## Font::get_EmphasisMark method


获取或设置应用于此格式的强调标记。

```cpp
Aspose::Words::EmphasisMark Aspose::Words::Font::get_EmphasisMark()
```


## 示例



展示如何在字形字符的上方/下方添加额外字符。
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// 可能的强调标记类型：
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder->get_Font()->set_EmphasisMark(emphasisMark);

builder->Write(u"Emphasis text");
builder->Writeln();
builder->get_Font()->ClearFormatting();
builder->Write(u"Simple text");

builder->get_Document()->Save(get_ArtifactsDir() + u"Fonts.SetEmphasisMark.docx");
```

## 另见

* Enum [EmphasisMark](../../emphasismark/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
