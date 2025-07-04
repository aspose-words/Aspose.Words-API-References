---
title: Aspose::Words::Lists::ListFormat class
linktitle: ListFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Lists::ListFormat class. Allows to control what list formatting is applied to a paragraph. To learn more, visit the  documentation article in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.lists/listformat/
---
## ListFormat class


Allows to control what list formatting is applied to a paragraph. To learn more, visit the [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/) documentation article.

```cpp
class ListFormat : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [ApplyBulletDefault](./applybulletdefault/)() | Starts a new default bulleted list and applies it to the paragraph. |
| [ApplyNumberDefault](./applynumberdefault/)() | Starts a new default numbered list and applies it to the paragraph. |
| [get_IsListItem](./get_islistitem/)() | True when the paragraph has bulleted or numbered formatting applied to it. |
| [get_List](./get_list/)() | Gets or sets the list this paragraph is a member of. |
| [get_ListLevel](./get_listlevel/)() | Returns the list level formatting plus any formatting overrides applied to the current paragraph. |
| [get_ListLevelNumber](./get_listlevelnumber/)() | Gets or sets the list level number (0 to 8) for the paragraph. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ListIndent](./listindent/)() | Increases the list level of the current paragraph by one level. |
| [ListOutdent](./listoutdent/)() | Decreases the list level of the current paragraph by one level. |
| [RemoveNumbers](./removenumbers/)() | Removes numbers or bullets from the current paragraph and sets list level to zero. |
| [set_List](./set_list/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Setter for [Aspose::Words::Lists::ListFormat::get_List](./get_list/). |
| [set_ListLevelNumber](./set_listlevelnumber/)(int32_t) | Setter for [Aspose::Words::Lists::ListFormat::get_ListLevelNumber](./get_listlevelnumber/). |
| static [Type](./type/)() |  |
## Remarks


A paragraph in a Microsoft Word document can be bulleted or numbered. When a paragraph is bulleted or numbered, it is said that list formatting is applied to the paragraph.

You do not create objects of the [ListFormat](./) class directly. You access [ListFormat](./) as a property of another object that can have list formatting associated with it. At the moment the objects that can have list formatting are: [Paragraph](../../aspose.words/paragraph/), [Style](../../aspose.words/style/) and [DocumentBuilder](../../aspose.words/documentbuilder/).

[ListFormat](./) of a [Paragraph](../../aspose.words/paragraph/) specifies what list formatting and list level is applied to that particular paragraph.

[ListFormat](./) of a [Style](../../aspose.words/style/) (applicable to paragraph styles only) allows to specify what list formatting and list level is applied to all paragraphs of that particular style.

[ListFormat](./) of a [DocumentBuilder](../../aspose.words/documentbuilder/) provides access to the list formatting at the current cursor position inside the [DocumentBuilder](../../aspose.words/documentbuilder/).

The list formatting itself is stored inside a [List](../list/) object that is stored separately from the paragraphs. The list objects are stored inside a [ListCollection](../listcollection/) collection. There is a single [ListCollection](../listcollection/) collection per [Document](../../aspose.words/document/).

The paragraphs do not physically belong to a list. The paragraphs just reference a particular list object via the [List](./get_list/) property and a particular level in the list via the [ListLevelNumber](./get_listlevelnumber/) property. By setting these two properties you control what bullets and numbering is applied to a paragraph.

## Examples



Shows how to work with list levels. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level.
// We can begin and end a list by using a document builder's "ListFormat" property.
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Below are two types of lists that we can create using a document builder.
// 1 -  A numbered list:
// Numbered lists create a logical order for their paragraphs by numbering each item.
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault));

ASSERT_TRUE(builder->get_ListFormat()->get_IsListItem());

// By setting the "ListLevelNumber" property, we can increase the list level
// to begin a self-contained sub-list at the current list item.
// The Microsoft Word list template called "NumberDefault" uses numbers to create list levels for the first list level.
// Deeper list levels use letters and lowercase Roman numerals.
for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// 2 -  A bulleted list:
// This list will apply an indent and a bullet symbol ("•") before each paragraph.
// Deeper levels of this list will use different symbols, such as "■" and "○".
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));

for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// We can disable list formatting to not format any subsequent paragraphs as lists by un-setting the "List" flag.
builder->get_ListFormat()->set_List(nullptr);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

doc->Save(get_ArtifactsDir() + u"Lists.SpecifyListLevel.docx");
```

## See Also

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
