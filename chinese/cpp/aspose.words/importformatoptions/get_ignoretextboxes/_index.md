---
title: "Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes 方法"
linktitle: "get_IgnoreTextBoxes"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes 方法。获取或设置一个布尔值，用于指定在使用 KeepSourceFormatting 模式时是否忽略文本框内容的源格式。默认值在 C++ 中为 true。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words/importformatoptions/get_ignoretextboxes/
---
## ImportFormatOptions::get_IgnoreTextBoxes method


获取或设置一个布尔值，用于指定在使用 [KeepSourceFormatting](../../importformatmode/) 模式时是否忽略文本框内容的源格式。默认值为 **true**。

```cpp
bool Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes() const
```


## 示例



展示如何在追加文档时管理文本框的格式。
```cpp
// 创建一个文档，将从另一个文档插入的节点放入其中。
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);

builder->Writeln(u"Hello world!");

// 创建另一个包含文本框的文档，我们将其导入到第一个文档中。
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBox = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 100);
builder->MoveTo(textBox->get_FirstParagraph());
builder->get_ParagraphFormat()->get_Style()->get_Font()->set_Name(u"Courier New");
builder->get_ParagraphFormat()->get_Style()->get_Font()->set_Size(24);
builder->Write(u"Textbox contents");

// 设置一个标志，以指定是清除还是保留文本框的格式
// 在将它们导入到其他文档时。
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_IgnoreTextBoxes(ignoreTextBoxes);

// 将文本框从源文档导入到目标文档，
// 然后验证我们是否保留了其文本内容的样式。
auto importer = System::MakeObject<Aspose::Words::NodeImporter>(srcDoc, dstDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, importFormatOptions);
auto importedTextBox = System::ExplicitCast<Aspose::Words::Drawing::Shape>(importer->ImportNode(textBox, true));
dstDoc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedTextBox);

if (ignoreTextBoxes)
{
    ASPOSE_ASSERT_EQ(12.0, importedTextBox->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Size());
    ASSERT_EQ(u"Times New Roman", importedTextBox->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());
}
else
{
    ASPOSE_ASSERT_EQ(24.0, importedTextBox->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Size());
    ASSERT_EQ(u"Courier New", importedTextBox->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());
}

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.IgnoreTextBoxes.docx");
```

## 另见

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
