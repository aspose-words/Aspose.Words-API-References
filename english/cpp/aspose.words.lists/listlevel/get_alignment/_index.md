---
title: Aspose::Words::Lists::ListLevel::get_Alignment method
linktitle: get_Alignment
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Lists::ListLevel::get_Alignment method. Gets or sets the justification of the actual number of the list item in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.lists/listlevel/get_alignment/
---
## ListLevel::get_Alignment method


Gets or sets the justification of the actual number of the list item.

```cpp
Aspose::Words::Lists::ListLevelAlignment Aspose::Words::Lists::ListLevel::get_Alignment() const
```

## Remarks


The list label is justified relative to the [NumberPosition](../get_numberposition/) property.

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

## See Also

* Enum [ListLevelAlignment](../../listlevelalignment/)
* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
