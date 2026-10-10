---
title: "Aspose::Words::Saving::XpsSaveOptions::get_OutlineOptions 方法"
linktitle: "get_OutlineOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::XpsSaveOptions::get_OutlineOptions 方法。允许在 C++ 中指定大纲选项。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.saving/xpssaveoptions/get_outlineoptions/
---
## XpsSaveOptions::get_OutlineOptions method


允许指定大纲选项。

```cpp
System::SharedPtr<Aspose::Words::Saving::OutlineOptions> Aspose::Words::Saving::XpsSaveOptions::get_OutlineOptions() const
```

## 备注


请注意，保存为 XPS 时，[ExpandedOutlineLevels](../../outlineoptions/get_expandedoutlinelevels/) 选项将不起作用。

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

* Class [OutlineOptions](../../outlineoptions/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
