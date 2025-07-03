---
title: Aspose::Words::Lists::ListCollection::AddCopy method
linktitle: AddCopy
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Lists::ListCollection::AddCopy method. Creates a new list by copying the specified list and adding it to the collection of lists in the document in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.lists/listcollection/addcopy/
---
## ListCollection::AddCopy method


Creates a new list by copying the specified list and adding it to the collection of lists in the document.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::AddCopy(const System::SharedPtr<Aspose::Words::Lists::List> &srcList)
```


| Parameter | Type | Description |
| --- | --- | --- |
| srcList | const System::SharedPtr\<Aspose::Words::Lists::List\>\& | The source list to copy from. |

### ReturnValue

The newly created list.
## Remarks


The source list can be from any document. If the source list belongs to a different document, a copy of the list is created and added to the current document.

If the source list is a reference to or a definition of a list style, the newly created list is not related to the original list style.

## Examples



Shows how to restart numbering in a list by copying a list. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level.
// We can begin and end a list by using a document builder's "ListFormat" property.
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Create a list from a Microsoft Word template, and customize its first list level.
System::SharedPtr<Aspose::Words::Lists::List> list1 = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberArabicParenthesis);
list1->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Red());
list1->get_ListLevels()->idx_get(0)->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);

// Apply our list to some paragraphs.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"List 1 starts below:");
builder->get_ListFormat()->set_List(list1);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// We can add a copy of an existing list to the document's list collection
// to create a similar list without making changes to the original.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->AddCopy(list1);
list2->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Blue());
list2->get_ListLevels()->idx_get(0)->set_StartAt(10);

// Apply the second list to new paragraphs.
builder->Writeln(u"List 2 starts below:");
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.RestartNumberingUsingListCopy.docx");
```

## See Also

* Class [List](../../list/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
