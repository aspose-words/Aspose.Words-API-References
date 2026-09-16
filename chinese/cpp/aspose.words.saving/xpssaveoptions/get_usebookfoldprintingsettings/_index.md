---
title: "Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings 方法"
linktitle: "get_UseBookFoldPrintingSettings"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings 方法。获取或设置一个布尔值，指示文档是否应使用小册子打印布局进行保存（如果在 C++ 中通过 MultiplePages 指定）。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.saving/xpssaveoptions/get_usebookfoldprintingsettings/
---
## XpsSaveOptions::get_UseBookFoldPrintingSettings method


获取或设置一个布尔值，指示文档是否应使用小册子打印布局进行保存（如果通过 [MultiplePages](../../../aspose.words/pagesetup/get_multiplepages/) 指定）。

```cpp
bool Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings() const
```

## 备注


如果指定此选项，保存时将忽略 [PageSet](../../fixedpagesaveoptions/get_pageset/)。此行为与 MS Word 相匹配。如果页面设置中未指定小册子打印设置，则此选项无效。

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

* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
