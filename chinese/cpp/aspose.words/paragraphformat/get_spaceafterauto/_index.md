---
title: "Aspose::Words::ParagraphFormat::get_SpaceAfterAuto 方法"
linktitle: "get_SpaceAfterAuto"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphFormat::get_SpaceAfterAuto 方法。如果段落后面的间距量在 C++ 中被自动设置，则为 true。"
type: docs
weight: 32000
url: /zh/cpp/aspose.words/paragraphformat/get_spaceafterauto/
---
## ParagraphFormat::get_SpaceAfterAuto method


如果段落之后的间距量是自动设置的，则为 True。

```cpp
bool Aspose::Words::ParagraphFormat::get_SpaceAfterAuto()
```

## 备注


当设置为 **true** 时，覆盖 [SpaceAfter](../get_spaceafter/) 的效果。

当您将段落的 Space Before 和 Space After 设置为 Auto 时，**Microsoft** Word 会根据以下规则自动在段落之间添加 14 磅的间距：

* Normally, spacing is added after all paragraphs.
* In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
* In a nested bulleted or numbered list spacing is not added.
* Spacing is normally added after a table.
* Spacing is not added after a table if it is the last block in a table cell.
* Spacing is not added after the last paragraph in a table cell.



## 示例



展示如何设置自动段落间距。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 在此生成器将创建的段落前后应用大量间距。
builder->get_ParagraphFormat()->set_SpaceBefore(24);
builder->get_ParagraphFormat()->set_SpaceAfter(24);

// 将这些标志设置为 "true" 以应用自动间距，
// 实际上会忽略我们上面设置的属性中的间距。
// 将它们保留为 "false" 将应用我们的自定义段落间距。
builder->get_ParagraphFormat()->set_SpaceAfterAuto(autoSpacing);
builder->get_ParagraphFormat()->set_SpaceBeforeAuto(autoSpacing);

// 插入两个段落，使其上下都有间距，并保存文档。
builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphSpacingAuto.docx");
```

## 另见

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
