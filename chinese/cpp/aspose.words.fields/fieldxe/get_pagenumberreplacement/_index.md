---
title: "Aspose::Words::Fields::FieldXE::get_PageNumberReplacement 方法"
linktitle: "get_PageNumberReplacement"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldXE::get_PageNumberReplacement 方法。获取或设置在 C++ 中用于替代页码的文本。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.fields/fieldxe/get_pagenumberreplacement/
---
## FieldXE::get_PageNumberReplacement method


获取或设置用于替代页码的文本。

```cpp
System::String Aspose::Words::Fields::FieldXE::get_PageNumberReplacement()
```


## 示例



展示如何在 INDEX 字段中定义交叉引用。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 创建一个 INDEX 字段，该字段将为文档中找到的每个 XE 字段显示一个条目。
// 每个条目将在左侧显示 XE 字段的 Text 属性值，
// 并在右侧显示包含 XE 字段的页码。
// INDEX 条目将收集所有在 "Text" 属性中具有匹配值的 XE 字段。
// 合并为一个条目，而不是为每个 XE 字段创建单独的条目。
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// 我们可以配置 XE 字段，使其 INDEX 条目显示字符串而不是页码。
// 首先，对于将页码替换为字符串的条目，
// 指定 XE 字段的 Text 属性值与字符串之间的自定义分隔符。
index->set_CrossReferenceSeparator(u", see: ");

ASSERT_EQ(u" INDEX  \\k \", see: \"", index->GetFieldCode());

// 插入一个 XE 字段，它会创建一个常规的 INDEX 条目，显示该字段的页码，
// 且不会调用 CrossReferenceSeparator 的值。
// 此 XE 字段的条目将显示 "Apple, 2"。
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apple");

ASSERT_EQ(u" XE  Apple", indexEntry->GetFieldCode());

// 在第 3 页插入另一个 XE 字段，并为 PageNumberReplacement 属性设置一个值。
// 该值将显示在该字段所在页的页码位置，
// 并且 INDEX 字段的 CrossReferenceSeparator 值会出现在它前面。
// 此 XE 字段的条目将显示 "Banana, see: Tropical fruit"。
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Banana");
indexEntry->set_PageNumberReplacement(u"Tropical fruit");

ASSERT_EQ(u" XE  Banana \\t \"Tropical fruit\"", indexEntry->GetFieldCode());

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.CrossReferenceSeparator.docx");
```

## 另见

* Class [FieldXE](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
