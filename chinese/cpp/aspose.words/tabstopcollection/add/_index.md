---
title: "Aspose::Words::TabStopCollection::Add method"
linktitle: "Add"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TabStopCollection::Add method. 在 C++ 中向集合中添加或替换制表位。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words/tabstopcollection/add/
---
## TabStopCollection::Add(const System::SharedPtr\<Aspose::Words::TabStop\>\&) method


在集合中添加或替换制表位。

```cpp
void Aspose::Words::TabStopCollection::Add(const System::SharedPtr<Aspose::Words::TabStop> &tabStop)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| tabStop | const System::SharedPtr\<Aspose::Words::TabStop\>\& | 要添加的制表位对象。 |
## 备注


如果在指定位置已经存在制表位，则会被替换。

## 示例



展示如何向文档添加自定义制表位。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// 下面介绍两种通过 "ParagraphFormat" 属性向段落的制表位集合添加制表位的方法。
// 1 - 创建一个 "TabStop" 对象，然后将其添加到集合中：
auto tabStop = System::MakeObject<Aspose::Words::TabStop>(Aspose::Words::ConvertUtil::InchToPoint(3), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
paragraph->get_ParagraphFormat()->get_TabStops()->Add(tabStop);

// 2 - 将新制表位属性的值传递给 "Add" 方法：
paragraph->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(100), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// 向所有段落添加 5 cm 的制表位。
for (auto&& para : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()))
{
    para->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(50), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
}

// 每个"tab"字符会将构建器的光标移动到下一个制表位的位置。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc->Save(get_ArtifactsDir() + u"TabStopCollection.AddTabStops.docx");
```

## 另见

* Class [TabStop](../../tabstop/)
* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## TabStopCollection::Add(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) method


在集合中添加或替换制表位。

```cpp
void Aspose::Words::TabStopCollection::Add(double position, Aspose::Words::TabAlignment alignment, Aspose::Words::TabLeader leader)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 位置 | double | 添加制表位的位置（以点为单位）。 |
| alignment | Aspose::Words::TabAlignment | 一个 [TabAlignment](../../tabalignment/) 值，用于指定制表位处文本的对齐方式。 |
| leader | Aspose::Words::TabLeader | 一个 [TabLeader](../../tableader/) 值，用于指定制表符下显示的前导线类型。 |
## 备注


如果在指定位置已经存在制表位，则会被替换。

## 示例



展示如何向文档添加自定义制表位。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// 下面介绍两种通过 "ParagraphFormat" 属性向段落的制表位集合添加制表位的方法。
// 1 - 创建一个 "TabStop" 对象，然后将其添加到集合中：
auto tabStop = System::MakeObject<Aspose::Words::TabStop>(Aspose::Words::ConvertUtil::InchToPoint(3), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
paragraph->get_ParagraphFormat()->get_TabStops()->Add(tabStop);

// 2 - 将新制表位属性的值传递给 "Add" 方法：
paragraph->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(100), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// 向所有段落添加 5 cm 的制表位。
for (auto&& para : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()))
{
    para->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(50), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
}

// 每个"tab"字符会将构建器的光标移动到下一个制表位的位置。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc->Save(get_ArtifactsDir() + u"TabStopCollection.AddTabStops.docx");
```

## 另见

* Enum [TabAlignment](../../tabalignment/)
* Enum [TabLeader](../../tableader/)
* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
