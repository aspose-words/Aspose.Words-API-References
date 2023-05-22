---
title: Aspose::Words::Lists::ListFormat::get_IsListItem method
linktitle: get_IsListItem
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Lists::ListFormat::get_IsListItem method. True when the paragraph has bulleted or numbered formatting applied to it in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.lists/listformat/get_islistitem/
---
## ListFormat::get_IsListItem method


True when the paragraph has bulleted or numbered formatting applied to it.

```cpp
bool Aspose::Words::Lists::ListFormat::get_IsListItem()
```


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


Shows how to output all paragraphs in a document that are list items. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Numbered list item 1");
builder->Writeln(u"Numbered list item 2");
builder->Writeln(u"Numbered list item 3");
builder->get_ListFormat()->RemoveNumbers();

builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Bulleted list item 1");
builder->Writeln(u"Bulleted list item 2");
builder->Writeln(u"Bulleted list item 3");
builder->get_ListFormat()->RemoveNumbers();

SharedPtr<NodeCollection> paras = doc->GetChildNodes(NodeType::Paragraph, true);

for (auto para : System::IterateOver(
         paras->LINQ_OfType<SharedPtr<Paragraph>>()->LINQ_Where([](SharedPtr<Paragraph> p) { return p->get_ListFormat()->get_IsListItem(); })))
{
    std::cout << String::Format(u"This paragraph belongs to list ID# {0}, number style \"{1}\"", para->get_ListFormat()->get_List()->get_ListId(),
                                para->get_ListFormat()->get_ListLevel()->get_NumberStyle())
              << std::endl;
    std::cout << "\t\"" << para->GetText().Trim() << "\"" << std::endl;
}
```

## See Also

* Class [ListFormat](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
