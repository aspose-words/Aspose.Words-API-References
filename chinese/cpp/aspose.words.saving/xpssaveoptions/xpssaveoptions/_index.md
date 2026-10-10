---
title: "Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions constructor"
linktitle: "XpsSaveOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions constructor. 初始化此类的新实例，可用于在 C++ 中以 Xps 格式保存文档。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.saving/xpssaveoptions/xpssaveoptions/
---
## XpsSaveOptions::XpsSaveOptions() constructor


初始化此类的新实例，可用于以 [Xps](../../../aspose.words/saveformat/) 格式保存文档。

```cpp
Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions()
```


## 示例



展示如何限制在已保存的 XPS 文档大纲中出现的标题级别。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入可作为目录条目的标题，级别为 1、2，然后是 3。
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsHeading());

builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);

builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);

builder->Writeln(u"Heading 1.2.1");
builder->Writeln(u"Heading 1.2.2");

// 创建一个 "XpsSaveOptions" 对象，以便我们可以将其传递给文档的 "Save" 方法
// 以修改该方法将文档转换为 .XPS 的方式。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Xps, saveOptions->get_SaveFormat());

// 输出的 XPS 文档将包含大纲，即列出文档正文中标题的目录。
// 单击此大纲中的条目将带我们定位到相应标题的位置。
// 将 "HeadingsOutlineLevels" 属性设置为 "2"，以从大纲中排除所有级别高于 2 的标题。
// 我们上面插入的最后两个标题将不会出现。
saveOptions->get_OutlineOptions()->set_HeadingsOutlineLevels(2);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

## 另见

* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## XpsSaveOptions::XpsSaveOptions(Aspose::Words::SaveFormat) constructor


初始化此类的新实例，可用于以 [Xps](../../../aspose.words/saveformat/) 或 [OpenXps](../../../aspose.words/saveformat/) 格式保存文档。

```cpp
Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


## 示例



展示如何将文档保存为 XPS 格式的书册折叠形式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

// 创建一个 "XpsSaveOptions" 对象，以便我们可以将其传递给文档的 "Save" 方法
// 以修改该方法将文档转换为 .XPS 的方式。
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>(Aspose::Words::SaveFormat::Xps);

// 将 \"UseBookFoldPrintingSettings\" 属性设置为 \"true\" 以排列内容
// 以一种有助于我们制作小册子的方式输出 XPS。
// 将 "UseBookFoldPrintingSettings" 属性设置为 "false" 以正常渲染 XPS。
xpsOptions->set_UseBookFoldPrintingSettings(renderTextAsBookFold);

// 如果我们将文档渲染为小册子，则必须设置 \"MultiplePages\"
// 所有章节的页面设置对象的属性为 \"MultiplePagesType.BookFoldPrinting\"。
if (renderTextAsBookFold)
{
    for (auto&& s : System::IterateOver<Aspose::Words::Section>(doc->get_Sections()))
    {
        s->get_PageSetup()->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);
    }
}

// 一旦打印此文档，我们可以通过堆叠页面将其制成小册子
// 从打印机出来后在中间折叠。
doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.BookFold.xps", xpsOptions);
```

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
