---
title: Aspose::Words::Lists::ListLevelAlignment enum
linktitle: ListLevelAlignment
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Lists::ListLevelAlignment enum. Specifies alignment for the list number or bullet in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.lists/listlevelalignment/
---
## ListLevelAlignment enum


Specifies alignment for the list number or bullet.

```cpp
enum class ListLevelAlignment
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Left | 0 | The list label is aligned to the left of the number position. |
| Center | 1 | The list label is centered at the number position. |
| Right | 2 | This list label is aligned to the right of the number position. |

## Remarks


Used as a value for the [Alignment](../listlevel/get_alignment/) property.

## Examples



Shows how to apply custom list formatting to paragraphs when using [DocumentBuilder](../../aspose.words/documentbuilder/). 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level.
// We can begin and end a list by using a document builder's "ListFormat" property.
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Create a list from a Microsoft Word template, and customize the first two of its list levels.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// This NumberFormat value will create star-shaped bullet list symbols.
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(Aspose::Words::Lists::ListTrailingCharacter::Space);
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
