---
title: "Aspose::Words::ImportFormatOptions::get_ForceCopyStyles 方法"
linktitle: "get_ForceCopyStyles"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ImportFormatOptions::get_ForceCopyStyles 方法。获取或设置一个布尔值，指示是否在 KeepSourceFormatting 模式下复制冲突的样式。默认值在 C++ 中为 false。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/importformatoptions/get_forcecopystyles/
---
## ImportFormatOptions::get_ForceCopyStyles method


获取或设置一个布尔值，指示是否在 [KeepSourceFormatting](../../importformatmode/) 模式下复制冲突的样式。默认值为 **false**。

```cpp
bool Aspose::Words::ImportFormatOptions::get_ForceCopyStyles() const
```

## 备注


默认情况下，如果目标文档中已经存在匹配的样式，源样式的格式将展开为直接节点属性，并且该节点的样式将重置为默认值。

当此选项设置为 **true** 时，源样式将被强制复制到目标文档，并使用唯一名称应用于导入的节点。

注意，在这种情况下，无法保证目标文档中导入节点的格式会被保留。

## 示例



展示如何强制复制具有唯一名称的源样式。
```cpp
// 两个文档都包含 MyStyle1 和 MyStyle2，MyStyle3 仅存在于源文档中。
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Styles source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Styles destination.docx");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ForceCopyStyles(true);
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

System::SharedPtr<Aspose::Words::ParagraphCollection> paras = dstDoc->get_Sections()->idx_get(1)->get_Body()->get_Paragraphs();

ASSERT_EQ(paras->idx_get(0)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle1_0");
ASSERT_EQ(paras->idx_get(1)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle2_0");
ASSERT_EQ(paras->idx_get(2)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle3");
```

## 另见

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
