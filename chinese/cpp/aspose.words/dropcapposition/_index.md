---
title: "Aspose::Words::DropCapPosition 枚举"
linktitle: "DropCapPosition"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DropCapPosition 枚举。指定 C++ 中首字下沉文本的位置。"
type: docs
weight: 87000
url: /zh/cpp/aspose.words/dropcapposition/
---
## DropCapPosition enum


指定首字下沉文字的位置。

```cpp
enum class DropCapPosition
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 | 该段落没有首字下沉。 |
| 普通 | 1 | 首字下沉位于锚点段落的文本边距内部。 |
| 边距 | 2 | 首字下沉位于锚点段落的文本边距外部。 |


## 示例



展示如何创建首字下沉。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入一个段落，其中包含一个大写字母，作为第二段和第三段文本的起始字符。
builder->get_Font()->set_Size(54);
builder->Writeln(u"L");

builder->get_Font()->set_Size(18);
builder->Writeln(System::String(u"orem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder->Writeln(System::String(u"Ut enim ad minim veniam, quis nostrud exercitation ") + u"ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// 当前，第二段和第三段将显示在第一段之下。
// 我们可以通过其 "ParagraphFormat" 对象将第一段转换为其他段落的首字母下沉。
// 将 "DropCapPosition" 属性设置为 "DropCapPosition.Margin" 以放置首字母下沉
// 在左侧页面边距之外（如果我们的文本从左到右）。
// 将 "DropCapPosition" 属性设置为 "DropCapPosition.Normal" 以将首字母下沉放置在页面边距内
// 并使其余文本环绕它。
// "DropCapPosition.None" 是所有段落的默认状态。
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();
format->set_DropCapPosition(dropCapPosition);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.DropCap.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
