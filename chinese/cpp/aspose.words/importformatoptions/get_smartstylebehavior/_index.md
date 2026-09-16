---
title: "Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior 方法"
linktitle: "get_SmartStyleBehavior"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior 方法。获取或设置一个布尔值，用于指定当源文档和目标文档中的样式名称相同​​时，样式将如何导入。默认值在 C++ 中为 false。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words/importformatoptions/get_smartstylebehavior/
---
## ImportFormatOptions::get_SmartStyleBehavior method


获取或设置一个布尔值，指定当源文档和目标文档的样式名称相同且冲突时，样式的导入方式。默认值为 **false**。

```cpp
bool Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior() const
```

## 备注


当此选项 **enabled** 时，如果使用 [KeepSourceFormatting](../../importformatmode/) 导入模式，源样式将展开为目标文档中的直接属性。

当此选项 **disabled** 时，只有在源样式带编号时才会展开。现有的目标属性（包括列表）将不会被覆盖。

## 示例



展示在插入文档时如何解决重复样式。
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);

System::SharedPtr<Aspose::Words::Style> myStyle = builder->get_Document()->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
myStyle->get_Font()->set_Size(14);
myStyle->get_Font()->set_Name(u"Courier New");
myStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

builder->get_ParagraphFormat()->set_StyleName(myStyle->get_Name());
builder->Writeln(u"Hello world!");

// 克隆文档并编辑克隆的 "MyStyle" 样式，使其颜色与原始文档不同。
// 如果我们将克隆插入原始文档，两个同名样式将导致冲突。
System::SharedPtr<Aspose::Words::Document> srcDoc = dstDoc->Clone();
srcDoc->get_Styles()->idx_get(u"MyStyle")->get_Font()->set_Color(System::Drawing::Color::get_Red());

// 当我们启用 SmartStyleBehavior 并使用 KeepSourceFormatting 导入格式模式时，
// Aspose.Words 将通过转换源文档的样式来解决样式冲突。
// 将与目标样式同名的样式转换为直接的段落属性。
auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_SmartStyleBehavior(true);

builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.SmartStyleBehavior.docx");
```

## 另见

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
