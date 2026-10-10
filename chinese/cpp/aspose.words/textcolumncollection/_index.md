---
title: "Aspose::Words::TextColumnCollection class"
linktitle: "TextColumnCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TextColumnCollection 类。一个 TextColumn 对象的集合，表示文档节中所有文本列。欲了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 71000
url: /zh/cpp/aspose.words/textcolumncollection/
---
## TextColumnCollection class


一个由 [TextColumn](../textcolumn/) 对象组成的集合，表示文档节中所有文本列。欲了解更多信息，请访问 [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/) 文档文章。

```cpp
class TextColumnCollection : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Count](./get_count/)() | 获取文档节中的列数。 |
| [get_EvenlySpaced](./get_evenlyspaced/)() | 如果文本列宽度相等且间距均匀，则为 True。 |
| [get_LineBetween](./get_linebetween/)() | 当 **true** 时，在列之间添加一条垂直线。 |
| [get_Spacing](./get_spacing/)() | 当列均匀间隔时，获取或设置每列之间的间距（单位：点）。 |
| [get_Width](./get_width/)() | 当列均匀间隔时，获取列的宽度。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | 返回指定索引处的文本列。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_EvenlySpaced](./set_evenlyspaced/)(bool) | 用于设置 [Aspose::Words::TextColumnCollection::get_EvenlySpaced](./get_evenlyspaced/) 的 setter。 |
| [set_LineBetween](./set_linebetween/)(bool) | 用于设置 [Aspose::Words::TextColumnCollection::get_LineBetween](./get_linebetween/) 的 setter。 |
| [set_Spacing](./set_spacing/)(double) | 用于设置 [Aspose::Words::TextColumnCollection::get_Spacing](./get_spacing/) 的 setter。 |
| [SetCount](./setcount/)(int32_t) | 将文本排列为指定数量的文本列。 |
| static [Type](./type/)() |  |
## 备注


使用 [SetCount()](./setcount/) 设置文本列的数量。

要使所有列宽度相等且均匀间隔，请将 [EvenlySpaced](./get_evenlyspaced/) 设置为 **true**，并在 [Spacing](./get_spacing/) 中指定列之间的间距。MS Word 将自动计算列宽。

如果将 [EvenlySpaced](./get_evenlyspaced/) 设置为 **false**，则需要为每列单独指定宽度和间距。使用索引器访问各个 [TextColumn](../textcolumn/) 对象。

使用自定义列宽时，请确保所有列宽及其之间的间距之和等于页面宽度减去左右页边距。

## 示例



展示如何在节中创建多个均匀间隔的列。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_Spacing(100);
columns->SetCount(2);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ColumnsSameWidth.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
