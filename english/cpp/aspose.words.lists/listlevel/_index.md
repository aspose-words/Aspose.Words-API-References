---
title: Aspose::Words::Lists::ListLevel class
linktitle: ListLevel
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Lists::ListLevel class. Defines formatting for a list level. To learn more, visit the Working with Lists documentation article in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.lists/listlevel/
---
## ListLevel class


Defines formatting for a list level. 
To learn more, visit the [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/) documentation article.

```cpp
class ListLevel : public IRunAttrSource
```

## Methods

| Method | Description |
| --- | --- |
| [CreatePictureBullet](./createpicturebullet/)() | Creates picture bullet shape for the current list level. |
| [DeletePictureBullet](./deletepicturebullet/)() | Deletes picture bullet for the current list level. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Lists::ListLevel\> \&) | Compares with the specified ListLevel. |
| static [GetEffectiveValue](./geteffectivevalue/)(int32_t, Aspose::Words::NumberStyle, const System::String \&) | Reports the string representation of the [ListLevel](./) object for the specified index of the list item. Parameters specify the [NumberStyle](../../aspose.words/numberstyle/) and an optional format string used when [Custom](../../aspose.words/numberstyle/) is specified. |
| [GetHashCode](./gethashcode/)() const override | Calculates hash code for this object. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| [RemoveTabStop](./removetabstop/)() | Removes tab stop from the list level. |
| static [Type](./type/)() |  |
| [get_Alignment](./get_alignment/)() const | Gets or sets the justification of the actual number of the list item. |
| [get_CustomNumberStyleFormat](./get_customnumberstyleformat/)() | Gets or sets the custom number style format for this list level. For example: "a, ç, ĝ, ...". |
| [get_Font](./get_font/)() | Specifies character formatting used for the list label. |
| [get_ImageData](./get_imagedata/)() | Returns image data of the picture bullet shape for the current list level. |
| [get_IsLegal](./get_islegal/)() const | True if the level turns all inherited numbers to Arabic, false if it preserves their number style. |
| [get_LinkedStyle](./get_linkedstyle/)() | Gets or sets the paragraph style that is linked to this list level. |
| [get_NumberFormat](./get_numberformat/)() const | Returns or sets the number format for the list level. |
| [get_NumberPosition](./get_numberposition/)() const | Returns or sets the position (in points) of the number or bullet for the list level. |
| [get_NumberStyle](./get_numberstyle/)() const | Returns or sets the number style for this list level. |
| [get_RestartAfterLevel](./get_restartafterlevel/)() const | Sets or returns the list level that must appear before the specified list level restarts numbering. |
| [get_StartAt](./get_startat/)() | Returns or sets the starting number for this list level. |
| [get_TabPosition](./get_tabposition/)() const | Returns or sets the tab position (in points) for the list level. |
| [get_TextPosition](./get_textposition/)() const | Returns or sets the position (in points) for the second line of wrapping text for the list level. |
| [get_TrailingCharacter](./get_trailingcharacter/)() const | Returns or sets the character inserted after the number for the list level. |
| [set_Alignment](./set_alignment/)(Aspose::Words::Lists::ListLevelAlignment) | Sets the justification of the actual number of the list item. |
| [set_CustomNumberStyleFormat](./set_customnumberstyleformat/)(const System::String \&) | Sets the custom number style format for this list level. For example: "a, ç, ĝ, ...". |
| [set_IsLegal](./set_islegal/)(bool) | True if the level turns all inherited numbers to Arabic, false if it preserves their number style. |
| [set_LinkedStyle](./set_linkedstyle/)(const System::SharedPtr\<Aspose::Words::Style\> \&) | Sets the paragraph style that is linked to this list level. |
| [set_NumberFormat](./set_numberformat/)(const System::String \&) | Sets the number format for the list level. |
| [set_NumberPosition](./set_numberposition/)(double) | Sets the position (in points) of the number or bullet for the list level. |
| [set_NumberStyle](./set_numberstyle/)(Aspose::Words::NumberStyle) | Sets the number style for this list level. |
| [set_RestartAfterLevel](./set_restartafterlevel/)(int32_t) | Sets or returns the list level that must appear before the specified list level restarts numbering. |
| [set_StartAt](./set_startat/)(int32_t) | Sets the starting number for this list level. |
| [set_TabPosition](./set_tabposition/)(double) | Sets the tab position (in points) for the list level. |
| [set_TextPosition](./set_textposition/)(double) | Sets the position (in points) for the second line of wrapping text for the list level. |
| [set_TrailingCharacter](./set_trailingcharacter/)(Aspose::Words::Lists::ListTrailingCharacter) | Sets the character inserted after the number for the list level. |
## Remarks


You do not create objects of this class. List level objects are created automatically when a list is created. You access [ListLevel](./) objects via the [ListLevelCollection](../listlevelcollection/) collection.

Use the properties of [ListLevel](./) to specify list formatting for individual list levels.
## Examples


Shows how to apply custom list formatting to paragraphs when using DocumentBuilder.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level.
// We can begin and end a list by using a document builder's "ListFormat" property.
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Create a list from a Microsoft Word template, and customize the first two of its list levels.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(ListLevelAlignment::Right);
listLevel->set_NumberStyle(NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// This NumberFormat value will create star-shaped bullet list symbols.
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// Create paragraphs and apply both list levels of our custom list formatting to them.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateCustomList.docx");
```
## See Also

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
