---
title: ListCollection
second_title: Aspose.Words for C++ API Reference
description: Stores and manages formatting of bulleted and numbered lists used in a document.
type: docs
weight: 14
url: /cpp/aspose.words.lists/listcollection/
---
## ListCollection class


Stores and manages formatting of bulleted and numbered lists used in a document.

```cpp
class ListCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Lists::List>>
```

## Methods

| Method | Description |
| --- | --- |
| [Add](./add/)(Aspose::Words::Lists::ListTemplate) | Creates a new list based on a predefined template and adds it to the collection of lists in the document. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Creates a new list that references a list style and adds it to the collection of lists in the document. |
| [AddCopy](./addcopy/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Creates a new list by copying the specified list and adding it to the collection of lists in the document. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Gets the count of numbered and bulleted lists in the document. |
| [get_Document](./get_document/)() const | Gets the owner document. |
| [GetEnumerator](./getenumerator/)() override | Gets the enumerator object that will enumerate lists in the document. |
| [GetListByListId](./getlistbylistid/)(int32_t) | Gets a list by a list identifier. |
| [idx_get](./idx_get/)(int32_t) | Gets a list by index. |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Description |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |

A list in a Microsoft Word document is a set of list formatting properties. The formatting of the lists is stored in the [ListCollection](./) collection separately from the paragraphs of text.

You do not create objects of this class. There is always only one [ListCollection](./) object per document and it is accessible via the [Lists](../../aspose.words/documentbase/get_lists/) property.

To create a new list based on a predefined list template or based on a list style, use the **Add()** method.

To create a new list with formatting identical to an existing list, use the **AddCopy()** method.

To make a paragraph bulleted or numbered, you need to apply list formatting to a paragraph by assigning a [List](../list/) object to the [List](../listformat/get_list/) property of [ListFormat](../listformat/).

To remove list formatting from a paragraph, use the [RemoveNumbers](../listformat/removenumbers/) method.

If you know a bit about WordprocessingML, then you might know it defines separate concepts for "list" and "list definition". This exactly corresponds to how list formatting is stored in a Microsoft Word document at the low level. [List](../list/) definition is like a "schema" and list is like an instance of a list definition.

To simplify programming model, Aspose.Words hides the distinction between list and list definition in much the same way like Microsoft Word hides this in its user interface. This allows you to concentrate more on how you want your document to look like, rather than building low-level objects to satisfy requirements of the Microsoft Word file format.

It is not possible to delete lists once they are created in the current version of [Aspose.Words](../../aspose.words/). This is similar to Microsoft Word where user does not have explicit control over list definitions.

## Examples




Shows how to work with list levels. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level.
// We can begin and end a list by using a document builder's "ListFormat" property.
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Below are two types of lists that we can create using a document builder.
// 1 -  A numbered list:
// Numbered lists create a logical order for their paragraphs by numbering each item.
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(ListTemplate::NumberDefault));

ASSERT_TRUE(builder->get_ListFormat()->get_IsListItem());

// By setting the "ListLevelNumber" property, we can increase the list level
// to begin a self-contained sub-list at the current list item.
// The Microsoft Word list template called "NumberDefault" uses numbers to create list levels for the first list level.
// Deeper list levels use letters and lowercase Roman numerals.
for (int i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(String(u"Level ") + i);
}

// 2 -  A bulleted list:
// This list will apply an indent and a bullet symbol ("•") before each paragraph.
// Deeper levels of this list will use different symbols, such as "■" and "○".
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(ListTemplate::BulletDefault));

for (int i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(String(u"Level ") + i);
}

// We can disable list formatting to not format any subsequent paragraphs as lists by un-setting the "List" flag.
builder->get_ListFormat()->set_List(nullptr);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

doc->Save(ArtifactsDir + u"Lists.SpecifyListLevel.docx");
```


Shows how to restart numbering in a list by copying a list. 
```cpp
auto doc = MakeObject<Document>();

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level.
// We can begin and end a list by using a document builder's "ListFormat" property.
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Create a list from a Microsoft Word template, and customize its first list level.
SharedPtr<List> list1 = doc->get_Lists()->Add(ListTemplate::NumberArabicParenthesis);
list1->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Red());
list1->get_ListLevels()->idx_get(0)->set_Alignment(ListLevelAlignment::Right);

// Apply our list to some paragraphs.
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"List 1 starts below:");
builder->get_ListFormat()->set_List(list1);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// We can add a copy of an existing list to the document's list collection
// to create a similar list without making changes to the original.
SharedPtr<List> list2 = doc->get_Lists()->AddCopy(list1);
list2->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Blue());
list2->get_ListLevels()->idx_get(0)->set_StartAt(10);

// Apply the second list to new paragraphs.
builder->Writeln(u"List 2 starts below:");
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

doc->Save(ArtifactsDir + u"Lists.RestartNumberingUsingListCopy.docx");
```


Shows how to create a document with a sample of all the lists from another document. 
```cpp
void PrintOutAllLists()
{
    auto srcDoc = MakeObject<Document>(MyDir + u"Rendering.docx");

    auto dstDoc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(dstDoc);

    for (const auto& srcList : srcDoc->get_Lists())
    {
        SharedPtr<List> dstList = dstDoc->get_Lists()->AddCopy(srcList);
        AddListSample(builder, dstList);
    }

    dstDoc->Save(ArtifactsDir + u"Lists.PrintOutAllLists.docx");
}

static void AddListSample(SharedPtr<DocumentBuilder> builder, SharedPtr<List> list)
{
    builder->Writeln(String(u"Sample formatting of list with ListId:") + list->get_ListId());
    builder->get_ListFormat()->set_List(list);
    for (int i = 0; i < list->get_ListLevels()->get_Count(); i++)
    {
        builder->get_ListFormat()->set_ListLevelNumber(i);
        builder->Writeln(String(u"Level ") + i);
    }

    builder->get_ListFormat()->RemoveNumbers();
    builder->Writeln();
}
```

