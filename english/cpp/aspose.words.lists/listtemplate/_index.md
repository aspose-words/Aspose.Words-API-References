---
title: ListTemplate
second_title: Aspose.Words for C++ API Reference
description: Specifies one of the predefined list formats available in Microsoft Word.
type: docs
weight: 92
url: /cpp/aspose.words.lists/listtemplate/
---
## ListTemplate enum


Specifies one of the predefined list formats available in Microsoft Word.

### Values

| Name | Value | Description |
| --- | --- | --- |
| BulletDefault | 0 | Default bulleted list with 9 levels. Bullet of the first level is a disc, bullet of the second level is a circle, bullet of the third level is a square. Then formatting repeats for the remaining levels. Each level is indented to the right by 0.25" relative to the previous level. Corresponds to the 1st bulleted list template in the Bullets and Numbering dialog box in Microsoft Word. |
| BulletDisk | n/a | Same as BulletDefault. Corresponds to the 1st bulleted list template in the Bullets and Numbering dialog box in Microsoft Word. |
| BulletCircle | n/a | The bullet of the first level is a circle. The remaining levels are same as in BulletDefault. Corresponds to the 2nd bulleted list template in the Bullets and Numbering dialog box in Microsoft Word. |
| BulletSquare | n/a | The bullet of the first level is a square. The remaining levels are same as in BulletDefault. Corresponds to the 3rd bulleted list template in the Bullets and Numbering dialog box in Microsoft Word. |
| BulletDiamonds | n/a | The bullet of the first level is a 4-diamond Wingding character. The remaining levels are same as in BulletDefault. Corresponds to the 5th bulleted list template in the Bullets and Numbering dialog box in Microsoft Word. |
| BulletArrowHead | n/a | The bullet of the first level is an arrow head Wingding character. The remaining levels are same as in BulletDefault. Corresponds to the 6th bulleted list template in the Bullets and Numbering dialog box in Microsoft Word. |
| BulletTick | n/a | The bullet of the first level is a tick Wingding character. The remaining levels are same as in BulletDefault. Corresponds to the 7th bulleted list template in the Bullets and Numbering dialog box in Microsoft Word. |
| NumberDefault | n/a | Default numbered list with 9 levels. Arabic numbering (1., 2., 3., ...) for the first level, lowercase letter numbering (a., b., c., ...) for the second level, lowercase roman numbering (i., ii., iii., ...) for the third level. Then formatting repeats for the remaining levels. Each level is indented to the right by 0.25" relative to the previous level. Corresponds to the 1st numbered list template in the Bullets and Numbering dialog box in Microsoft Word. |
| NumberArabicDot | n/a | Same as NumberDefault. Corresponds to the 1st numbered list template in the Bullets and Numbering dialog box in Microsoft Word. |
| NumberArabicParenthesis | n/a | The number of the first level is "1)". The remaining levels are same as in NumberDefault. Corresponds to the 2nd numbered list template in the Bullets and Numbering dialog box in Microsoft Word. |
| NumberUppercaseRomanDot | n/a | The number of the first level is "I.". The remaining levels are same as in NumberDefault. Corresponds to the 3rd numbered list template in the Bullets and Numbering dialog box in Microsoft Word. |
| NumberUppercaseLetterDot | n/a | The number of the first level is "A.". The remaining levels are same as in NumberDefault. Corresponds to the 4th numbered list template in the Bullets and Numbering dialog box in Microsoft Word. |
| NumberLowercaseLetterParenthesis | n/a | The number of the first level is "a)". The remaining levels are same as in NumberDefault. Corresponds to the 5th numbered list template in the Bullets and Numbering dialog box in Microsoft Word. |
| NumberLowercaseLetterDot | n/a | The number of the first level is "a.". The remaining levels are same as in NumberDefault. Corresponds to the 6th numbered list template in the Bullets and Numbering dialog box in Microsoft Word. |
| NumberLowercaseRomanDot | n/a | The number of the first level is "i.". The remaining levels are same as in NumberDefault. Corresponds to the 7th numbered list template in the Bullets and Numbering dialog box in Microsoft Word. |
| OutlineNumbers | n/a | An outline list with levels numbered "1), a), i), (1), (a), (i), 1., a., i.". Corresponds to the 1st outline list template in the Bullets and Numbering dialog box in Microsoft Word. |
| OutlineLegal | n/a | An outline list with levels are numbered "1., 1.1., 1.1.1, ...". Corresponds to the 2nd outline list template in the Bullets and Numbering dialog box in Microsoft Word. |
| OutlineBullets | n/a | An outline lists with various bullets for different levels. Corresponds to the 3rd outline list template in the Bullets and Numbering dialog box in Microsoft Word. |
| OutlineHeadingsArticleSection | n/a | An outline list with levels linked to Heading styles. Corresponds to the 4th outline list template in the Bullets and Numbering dialog box in Microsoft Word. |
| OutlineHeadingsLegal | n/a | An outline list with levels linked to Heading styles. Corresponds to the 5th outline list template in the Bullets and Numbering dialog box in Microsoft Word. |
| OutlineHeadingsNumbers | n/a | An outline list with levels linked to Heading styles. Corresponds to the 6th outline list template in the Bullets and Numbering dialog box in Microsoft Word. |
| OutlineHeadingsChapter | n/a | An outline list with levels linked to Heading styles. Corresponds to the 7th outline list template in the Bullets and Numbering dialog box in Microsoft Word. |


A list template value is used as a parameter into the [Add()](../listcollection/add/) method.

Aspose.Words list templates correspond to the 21 list templates available in the Bullets and Numbering dialog box in Microsoft Word 2003.

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


Shows how to create a document that contains all outline headings list templates. 
```cpp
void OutlineHeadingTemplates()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    SharedPtr<List> list = doc->get_Lists()->Add(ListTemplate::OutlineHeadingsArticleSection);
    AddOutlineHeadingParagraphs(builder, list, u"Aspose.Words Outline - \"Article Section\"");

    list = doc->get_Lists()->Add(ListTemplate::OutlineHeadingsLegal);
    AddOutlineHeadingParagraphs(builder, list, u"Aspose.Words Outline - \"Legal\"");

    builder->InsertBreak(BreakType::PageBreak);

    list = doc->get_Lists()->Add(ListTemplate::OutlineHeadingsNumbers);
    AddOutlineHeadingParagraphs(builder, list, u"Aspose.Words Outline - \"Numbers\"");

    list = doc->get_Lists()->Add(ListTemplate::OutlineHeadingsChapter);
    AddOutlineHeadingParagraphs(builder, list, u"Aspose.Words Outline - \"Chapters\"");

    doc->Save(ArtifactsDir + u"Lists.OutlineHeadingTemplates.docx");
}

static void AddOutlineHeadingParagraphs(SharedPtr<DocumentBuilder> builder, SharedPtr<List> list, String title)
{
    builder->get_ParagraphFormat()->ClearFormatting();
    builder->Writeln(title);

    for (int i = 0; i < 9; i++)
    {
        builder->get_ListFormat()->set_List(list);
        builder->get_ListFormat()->set_ListLevelNumber(i);

        String styleName = String(u"Heading ") + (i + 1);
        builder->get_ParagraphFormat()->set_StyleName(styleName);
        builder->Writeln(styleName);
    }

    builder->get_ListFormat()->RemoveNumbers();
}
```

