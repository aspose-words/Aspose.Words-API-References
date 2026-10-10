---
title: "Aspose::Words::ParagraphFormat::get_Bidi method"
linktitle: "get_Bidi"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphFormat::get_Bidi method. 获取或设置此段落是否为从右到左的段落（C++）。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words/paragraphformat/get_bidi/
---
## ParagraphFormat::get_Bidi method


获取或设置此段落是否为从右到左。

```cpp
bool Aspose::Words::ParagraphFormat::get_Bidi()
```

## 备注


当 **true** 时，此段落中的运行和其他内联对象将从右到左布局。

## 示例



展示如何使用 BIDIOUTLINE 字段创建兼容从右到左语言的列表。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// BIDIOUTLINE 字段对段落进行编号，类似于 AUTONUM/LISTNUM 字段，
// 但仅在启用了从右到左的编辑语言时可见，例如希伯来语或阿拉伯语。
// 以下字段将显示 ".1"，即列表编号 "1." 的 RTL 等价。
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBidiOutline>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true));
builder->Writeln(u"שלום");

ASSERT_EQ(u" BIDIOUTLINE ", field->GetFieldCode());

// 再添加两个 BIDIOUTLINE 字段，它们将显示 ".2" 和 ".3"。
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");

// 将文档中每个段落的水平文本对齐方式设置为 RTL。
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    para->get_ParagraphFormat()->set_Bidi(true);
}

// 如果在 Microsoft Word 中启用从右到左的编辑语言，我们的字段将显示数字。
// 否则，它们将显示 "###"。
doc->Save(get_ArtifactsDir() + u"Field.BIDIOUTLINE.docx");
```


展示如何检测纯文本文档的文本方向。
```cpp
// 创建一个 \"TxtLoadOptions\" 对象，以便我们可以将其传递给文档的构造函数
// 以修改加载纯文本文档的方式。
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// 将 \"DocumentDirection\" 属性设置为 \"DocumentDirection.Auto\"，自动检测
// Aspose.Words 从纯文本加载的每个段落的文本方向。
// 每个段落的 \"Bidi\" 属性将存储其方向。
loadOptions->set_DocumentDirection(Aspose::Words::Loading::DocumentDirection::Auto);

// 将希伯来文检测为从右到左。
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Hebrew text.txt", loadOptions);

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());

// 将英文检测为从右到左。
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());
```

## 另见

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
