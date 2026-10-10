---
title: "Aspose::Words::Inline::get_Font 方法"
linktitle: "get_Font"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Inline::get_Font 方法。提供对该对象的字体格式的访问（使用 C++）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words/inline/get_font/
---
## Inline::get_Font method


提供对该对象字体格式的访问。

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Inline::get_Font()
```


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

* Class [Font](../../font/)
* Class [Inline](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
