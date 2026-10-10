---
title: "Aspose::Words::EmphasisMark enum"
linktitle: "EmphasisMark"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::EmphasisMark 枚举。指定 C++ 中可能的强调标记类型。"
type: docs
weight: 89000
url: /zh/cpp/aspose.words/emphasismark/
---
## EmphasisMark enum


指定可能的强调标记类型。

```cpp
enum class EmphasisMark
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 | 无强调标记。 |
| OverSolidCircle | 1 | 强调标记是显示在文本上方的实心黑色圆圈。 |
| OverComma | 2 | 强调标记是显示在文本上方的逗号字符。 |
| OverWhiteCircle | 3 | 强调标记是显示在文本上方的空白白色圆圈。 |
| UnderSolidCircle | 4 | 强调标记是显示在文本下方的实心黑色圆圈。 |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
