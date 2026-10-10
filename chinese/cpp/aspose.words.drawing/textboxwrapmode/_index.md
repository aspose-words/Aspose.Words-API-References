---
title: "Aspose::Words::Drawing::TextBoxWrapMode 枚举"
linktitle: "TextBoxWrapMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::TextBoxWrapMode 枚举。指定在 C++ 中文本在形状内部的换行方式。"
type: docs
weight: 40000
url: /zh/cpp/aspose.words.drawing/textboxwrapmode/
---
## TextBoxWrapMode enum


指定文本在形状内部的换行方式。

```cpp
enum class TextBoxWrapMode
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Square | 0 | 文本在形状内部换行。 |
| None | 2 | 文本在形状内部不换行。 |


## 示例



展示如何为文本框的内容设置换行模式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 300);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// 将 "TextBoxWrapMode" 属性设置为 "TextBoxWrapMode.None" 以增加文本框的宽度
// 以容纳文本，前提是文本足够大。
// 将 "TextBoxWrapMode" 属性设置为 "TextBoxWrapMode.Square" 以
// 在文本框内部换行所有文本，同时保持其尺寸。
textBox->set_TextBoxWrapMode(textBoxWrapMode);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->get_Font()->set_Size(32);
builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxContentsWrapMode.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
