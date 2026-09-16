---
title: "Aspose::Words::ParagraphAlignment 枚举"
linktitle: "ParagraphAlignment"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphAlignment 枚举。指定 C++ 中段落的文本对齐方式。"
type: docs
weight: 110000
url: /zh/cpp/aspose.words/paragraphalignment/
---
## ParagraphAlignment enum


指定段落中的文本对齐方式。

```cpp
enum class ParagraphAlignment
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 左 | 0 | 文本左对齐。 |
| 居中 | 1 | 文本水平居中。 |
| 右 | 2 | 文本右对齐。 |
| 两端对齐 | 3 | 文本两端对齐。 |
| 分散 | 4 | 文本均匀分布。 |
| ArabicMediumKashida | 5 | 仅阿拉伯文。文本的Kashida长度延伸至由用户决定的中等长度。 |
| ArabicHighKashida | 7 | 仅阿拉伯文。文本的Kashida长度延伸至可能的最大长度。 |
| ArabicLowKashida | 8 | 仅阿拉伯文。文本的Kashida长度延伸至稍长的长度。 |
| ThaiDistributed | 9 | 仅泰文。文本已两端对齐，并针对泰文进行优化。 |
| MathElementCenterAsGroup | 10 | 行中唯一的 [Math](../../aspose.words.math/) 元素，按 'Centered As Group' 对齐。 |


## 示例



展示如何手动构建 Aspose.Words 文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 空白文档包含一个节、一个主体和一个段落。
// 调用 "RemoveAllChildren" 方法以删除所有这些节点，
// 最终得到一个没有子节点的文档节点。
doc->RemoveAllChildren();

// 此文档现在没有可用于添加内容的复合子节点。
// 如果我们想编辑它，需要重新填充其节点集合。
// 首先，创建一个新节，然后将其作为子节点追加到根文档节点。
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// 为该节设置一些页面布局属性。
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// 一个节需要一个主体，用于包含并显示其所有内容
// 在页面上位于该节的页眉和页脚之间。
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// 创建一个段落，设置一些格式属性，然后将其作为子节点追加到主体中。
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// 最后，添加一些内容以完成文档。创建一个运行（run），
// 设置其外观和内容，然后将其作为子节点追加到段落中。
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
