---
title: get_NumberStyle
second_title: Aspose.Words for C++ API Reference
description: Returns or sets the number style for this list level.
type: docs
weight: 170
url: /cpp/aspose.words.lists/listlevel/get_numberstyle/
---
## ListLevel::get_NumberStyle method


Returns or sets the number style for this list level.

```cpp
Aspose::Words::NumberStyle Aspose::Words::Lists::ListLevel::get_NumberStyle() const
```


## Examples



Shows how to apply custom list formatting to paragraphs when using [DocumentBuilder](../../../aspose.words/documentbuilder/). 
```cpp
auto doc = MakeObject<Document>();

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level.
// We can begin and end a list by using a document builder's "ListFormat" property.
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Create a list from a Microsoft Word template, and customize the first two of its list levels.
SharedPtr<List> list = doc->get_Lists()->Add(ListTemplate::NumberDefault);

SharedPtr<ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
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
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(ArtifactsDir + u"Lists.CreateCustomList.docx");
```


Shows advances ways of customizing list labels. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level.
// We can begin and end a list by using a document builder's "ListFormat" property.
// Each paragraph that we add between a list's start and the end will become an item in the list.
SharedPtr<List> list = doc->get_Lists()->Add(ListTemplate::NumberDefault);

// Level 1 labels will be formatted according to the "Heading 1" paragraph style and will have a prefix.
// These will look like "Appendix A", "Appendix B"...
list->get_ListLevels()->idx_get(0)->set_NumberFormat(u"Appendix \x0000");
list->get_ListLevels()->idx_get(0)->set_NumberStyle(NumberStyle::UppercaseLetter);
list->get_ListLevels()->idx_get(0)->set_LinkedStyle(doc->get_Styles()->idx_get(u"Heading 1"));

// Level 2 labels will display the current numbers of the first and the second list levels and have leading zeroes.
// If the first list level is at 1, then the list labels from these will look like "Section (1.01)", "Section (1.02)"...
list->get_ListLevels()->idx_get(1)->set_NumberFormat(u"Section (\x0000"
                                                     u".\x0001"
                                                     u")");
list->get_ListLevels()->idx_get(1)->set_NumberStyle(NumberStyle::LeadingZero);

// Note that the higher-level uses UppercaseLetter numbering.
// We can set the "IsLegal" property to use Arabic numbers for the higher list levels.
list->get_ListLevels()->idx_get(1)->set_IsLegal(true);
list->get_ListLevels()->idx_get(1)->set_RestartAfterLevel(0);

// Level 3 labels will be upper case Roman numerals with a prefix and a suffix and will restart at each List level 1 item.
// These list labels will look like "-I-", "-II-"...
list->get_ListLevels()->idx_get(2)->set_NumberFormat(u"-\x0002"
                                                     u"-");
list->get_ListLevels()->idx_get(2)->set_NumberStyle(NumberStyle::UppercaseRoman);
list->get_ListLevels()->idx_get(2)->set_RestartAfterLevel(1);

// Make labels of all list levels bold.
for (const auto& level : list->get_ListLevels())
{
    level->get_Font()->set_Bold(true);
}

// Apply list formatting to the current paragraph.
builder->get_ListFormat()->set_List(list);

// Create list items that will display all three of our list levels.
for (int n = 0; n < 2; n++)
{
    for (int i = 0; i < 3; i++)
    {
        builder->get_ListFormat()->set_ListLevelNumber(i);
        builder->Writeln(String(u"Level ") + i);
    }
}

builder->get_ListFormat()->RemoveNumbers();

doc->Save(ArtifactsDir + u"Lists.CreateListRestartAfterHigher.docx");
```

## See Also

* Enum [NumberStyle](../../../aspose.words/numberstyle/)
* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words](../../../)
