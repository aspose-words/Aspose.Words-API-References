---
title: "Aspose::Words::TabStopCollection class"
linktitle: "TabStopCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TabStopCollection class。一个包含 TabStop 对象的集合，这些对象表示段落或样式的自定义制表位。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 69000
url: /zh/cpp/aspose.words/tabstopcollection/
---
## TabStopCollection class


一个包含 [TabStop](../tabstop/) 对象的集合，这些对象表示段落或样式的自定义制表位。欲了解更多，请访问 [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) 文档文章。

```cpp
class TabStopCollection : public Aspose::Words::InternableComplexAttr,
                          public Aspose::Words::IExpandableAttr
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::TabStop\>\&) | 在集合中添加或替换制表位。 |
| [Add](./add/)(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) | 在集合中添加或替换制表位。 |
| [After](./after/)(double) | 获取指定位置右侧的第一个制表位。 |
| [Before](./before/)(double) | 获取指定位置左侧的第一个制表位。 |
| [Clear](./clear/)() | 删除所有制表位位置。 |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::TabStopCollection\>\&) | 确定指定的 [TabStopCollection](./) 在数值上是否等于当前的 [TabStopCollection](./)。 |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | 确定指定的对象在值上是否等于当前对象。 |
| [get_Count](./get_count/)() | 获取集合中制表位的数量。 |
| [GetHashCode](./gethashcode/)() const override | 作为此类型的哈希函数。 |
| [GetIndexByPosition](./getindexbyposition/)(double) | 获取具有指定点位置的制表位的索引。 |
| [GetPositionByIndex](./getpositionbyindex/)(int32_t) | 获取指定索引处制表位的位置（以点为单位）。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | 获取给定索引处的制表位。 |
| [idx_get](./idx_get/)(double) | 获取指定位置的制表位。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveByIndex](./removebyindex/)(int32_t) | 从集合中移除指定索引处的制表位。 |
| [RemoveByPosition](./removebyposition/)(double) | 从集合中移除指定位置的制表位。 |
| static [Type](./type/)() |  |
## 备注


在 Microsoft Word 文档中，制表位可以在段落样式的属性中或直接在段落的属性中定义。样式可以基于另一个样式。因此，给定对象的完整制表位集合是该对象直接定义的制表位与从父样式继承的制表位的组合。

在 Aspose.Words 中，当您获取段落或样式的 [TabStopCollection](./) 时，它仅包含直接为该段落或样式定义的自定义制表位。该集合不包括在父样式中定义的制表位或默认制表位。

## 示例



展示如何使用文档的制表位集合。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = builder->get_ParagraphFormat()->get_TabStops();

// 72 磅等于 Microsoft Word 制表位尺上的一个"英寸"。
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(72.0));
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(432.0, Aspose::Words::TabAlignment::Right, Aspose::Words::TabLeader::Dashes));

ASSERT_EQ(2, tabStops->get_Count());
ASSERT_FALSE(tabStops->idx_get(0)->get_IsClear());
ASSERT_FALSE(System::ObjectExt::Equals(tabStops->idx_get(0), tabStops->idx_get(1)));

// 每个"tab"字符会将构建器的光标移动到下一个制表位的位置。
builder->Writeln(u"Start\tTab 1\tTab 2");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(2, paragraphs->get_Count());

// 每个段落都有自己的制表位集合，该集合会从文档构建器的制表位集合克隆其值。
ASPOSE_ASSERT_EQ(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());
ASPOSE_ASSERT_NS(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());

// 制表位集合可以指向某些位置前后的制表位。
ASPOSE_ASSERT_EQ(72.0, tabStops->Before(100.0)->get_Position());
ASPOSE_ASSERT_EQ(432.0, tabStops->After(100.0)->get_Position());

// 我们可以清除段落的制表位集合，以恢复默认的制表行为。
paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->Clear();

ASSERT_EQ(0, paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->get_Count());

doc->Save(get_ArtifactsDir() + u"TabStopCollection.TabStopCollection.docx");
```

## 另见

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
