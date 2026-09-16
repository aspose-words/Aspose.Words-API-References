---
title: "Aspose::Words::Fields::FieldXE::get_Yomi 方法"
linktitle: "get_Yomi"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldXE::get_Yomi 方法。获取或设置索引条目的 yomi（用于排序索引的首个音标字符），在 C++ 中。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.fields/fieldxe/get_yomi/
---
## FieldXE::get_Yomi method


获取或设置索引条目的 yomi（用于索引排序的首个音标字符）。

```cpp
System::String Aspose::Words::Fields::FieldXE::get_Yomi()
```


## 示例



展示如何对 INDEX 字段条目进行音标排序。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 创建一个 INDEX 字段，该字段将为文档中找到的每个 XE 字段显示一个条目。
// 每个条目将在左侧显示 XE 字段的 Text 属性值，
// 并在右侧显示包含 XE 字段的页码。
// INDEX 条目将收集所有在 "Text" 属性中具有匹配值的 XE 字段。
// 合并为一个条目，而不是为每个 XE 字段创建单独的条目。
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// INDEX 表会自动按其 Text 属性的值以字母顺序对条目进行排序。
// 将 INDEX 表设置为使用平假名进行音标排序。
index->set_UseYomi(sortEntriesUsingYomi);

if (sortEntriesUsingYomi)
{
    ASSERT_EQ(u" INDEX  \\y", index->GetFieldCode());
}
else
{
    ASSERT_EQ(u" INDEX ", index->GetFieldCode());
}

// 插入 4 个 XE 字段，它们将在 INDEX 字段的目录中显示为条目。
// "Text" 属性可能包含汉字形式的单词拼写，其发音可能存在歧义，
// 而 "Yomi" 版本则会使用平假名准确拼写其发音。
// 如果我们将 INDEX 字段设置为使用 Yomi，它将对这些条目进行排序
// 依据它们的 Yomi 属性值，而不是 Text 属性值。
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"愛子");
indexEntry->set_Yomi(u"あ");

ASSERT_EQ(u" XE  愛子 \\y あ", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"明美");
indexEntry->set_Yomi(u"あ");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"恵美");
indexEntry->set_Yomi(u"え");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"愛美");
indexEntry->set_Yomi(u"え");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Yomi.docx");
```

## 另见

* Class [FieldXE](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
