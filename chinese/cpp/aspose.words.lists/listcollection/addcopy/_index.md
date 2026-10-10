---
title: "Aspose::Words::Lists::ListCollection::AddCopy 方法"
linktitle: "AddCopy"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Lists::ListCollection::AddCopy 方法。在 C++ 中通过复制指定的列表并将其添加到文档的列表集合中来创建一个新列表。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.lists/listcollection/addcopy/
---
## ListCollection::AddCopy method


通过复制指定的列表创建一个新列表，并将其添加到文档中的列表集合中。

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::AddCopy(const System::SharedPtr<Aspose::Words::Lists::List> &srcList)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| srcList | const System::SharedPtr\<Aspose::Words::Lists::List\>\& | 要复制的源列表。 |

### ReturnValue

新创建的列表。
## 备注


源列表可以来自任何文档。如果源列表属于不同的文档，则会创建该列表的副本并将其添加到当前文档中。

如果源列表是对列表样式的引用或定义，则新创建的列表与原始列表样式无关。

## 示例



演示如何通过复制列表来重新开始列表编号。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集合。
// 我们可以通过增加缩进级别来创建嵌套列表。
// 我们可以使用文档生成器的 "ListFormat" 属性来开始和结束列表。
// 我们在列表开始和结束之间添加的每个段落都会成为列表中的一项。
// 从 Microsoft Word 模板创建列表，并自定义其第一个列表级别。
System::SharedPtr<Aspose::Words::Lists::List> list1 = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberArabicParenthesis);
list1->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Red());
list1->get_ListLevels()->idx_get(0)->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);

// 将我们的列表应用于一些段落。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"List 1 starts below:");
builder->get_ListFormat()->set_List(list1);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// 我们可以将现有列表的副本添加到文档的列表集合中
// 以创建一个相似的列表而不更改原始列表。
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->AddCopy(list1);
list2->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Blue());
list2->get_ListLevels()->idx_get(0)->set_StartAt(10);

// 将第二个列表应用于新段落。
builder->Writeln(u"List 2 starts below:");
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.RestartNumberingUsingListCopy.docx");
```

## 另见

* Class [List](../../list/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
