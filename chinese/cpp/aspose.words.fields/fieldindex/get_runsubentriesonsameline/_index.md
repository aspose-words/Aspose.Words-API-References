---
title: "Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine 方法"
linktitle: "get_RunSubentriesOnSameLine"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine 方法。获取或设置在 C++ 中是否将子条目放在主条目的同一行。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words.fields/fieldindex/get_runsubentriesonsameline/
---
## FieldIndex::get_RunSubentriesOnSameLine method


获取或设置是否将子条目放在与主条目同一行。

```cpp
bool Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine()
```


## 示例



展示如何在 INDEX 字段中处理子条目。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 创建一个 INDEX 字段，该字段将为文档中找到的每个 XE 字段显示一个条目。
// 每个条目将在左侧显示 XE 字段的 Text 属性值，
// 并在右侧显示包含 XE 字段的页码。
// INDEX 条目将收集所有在 "Text" 属性中具有匹配值的 XE 字段。
// 合并为一个条目，而不是为每个 XE 字段创建单独的条目。
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));
index->set_PageNumberSeparator(u", see page ");
index->set_Heading(u"A");

// 具有 Text 属性且其值成为 INDEX 条目标题的 XE 字段。
// 如果此值包含由冒号分隔的两个字符串段（INDEX 条目将把 :) 视为分隔符），
// 第一个段是标题，第二个段将成为副标题。
// INDEX 字段首先按字母顺序对条目进行分组，然后，如果存在多个具有相同
// 标题，INDEX 字段将根据这些标题的值进一步对子项进行分组。
// 可以有多个子分组层，具体取决于出现的次数。
// XE 字段的 Text 属性会被分割成如下形式。
// 默认情况下，INDEX 字段条目组会为该组内的每个子标题创建一个新行。
// 我们可以将 RunSubentriesOnSameLine 标志设为 true，以保留标题，
// 并将该组的所有子标题放在同一行，这将使 INDEX 字段更紧凑。
index->set_RunSubentriesOnSameLine(runSubentriesOnTheSameLine);

if (runSubentriesOnTheSameLine)
{
    ASSERT_EQ(u" INDEX  \\e \", see page \" \\h A \\r", index->GetFieldCode());
}
else
{
    ASSERT_EQ(u" INDEX  \\e \", see page \" \\h A", index->GetFieldCode());
}

// 插入两个 XE 字段，每个位于新页面，并使用相同的标题 "Heading 1"，
// INDEX 字段将使用该标题对它们进行分组。
// 如果 RunSubentriesOnSameLine 为 false，则 INDEX 表将创建三行：
// 一行用于分组标题 "Heading 1"，每个子标题再各占一行。
// 如果 RunSubentriesOnSameLine 为 true，则 INDEX 表将创建一行
// 条目，包含标题及所有子标题。
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Heading 1:Subheading 1");

ASSERT_EQ(u" XE  \"Heading 1:Subheading 1\"", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Heading 1:Subheading 2");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + System::String::Format(u"Field.INDEX.XE.Subheading.docx"));
```

## 另见

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
