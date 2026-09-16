---
title: "Aspose::Words::TabStop::TabStop 构造函数"
linktitle: "TabStop"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TabStop::TabStop 构造函数。初始化此类在 C++ 中的新实例。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words/tabstop/tabstop/
---
## TabStop::TabStop(double) constructor


初始化此类的新实例。

```cpp
Aspose::Words::TabStop::TabStop(double position)
```


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

* Class [TabStop](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## TabStop::TabStop(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) constructor


初始化此类的新实例。

```cpp
Aspose::Words::TabStop::TabStop(double position, Aspose::Words::TabAlignment alignment, Aspose::Words::TabLeader leader)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 位置 | double | 制表位的点数位置。 |
| alignment | Aspose::Words::TabAlignment | 一个指定此制表位文本对齐方式的 [TabAlignment](../../tabalignment/) 值。 |
| leader | Aspose::Words::TabLeader | 一个 [TabLeader](../../tableader/) 值，用于指定制表符下显示的前导线类型。 |

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

* Enum [TabAlignment](../../tabalignment/)
* Enum [TabLeader](../../tableader/)
* Class [TabStop](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
