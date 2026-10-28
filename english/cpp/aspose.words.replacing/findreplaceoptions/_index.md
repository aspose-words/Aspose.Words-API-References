---
title: Aspose::Words::Replacing::FindReplaceOptions class
linktitle: FindReplaceOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Replacing::FindReplaceOptions class. Specifies options for find/replace operations. To learn more, visit the Find and Replace documentation article in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class


Specifies options for find/replace operations. 
To learn more, visit the [Find and Replace](https://docs.aspose.com/words/cpp/find-and-replace/) documentation article.

```cpp
class FindReplaceOptions : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [FindReplaceOptions](./findreplaceoptions/)() | Initializes a new instance of the FindReplaceOptions class with default settings. |
| [FindReplaceOptions](./findreplaceoptions/)(Aspose::Words::Replacing::FindReplaceDirection) | Initializes a new instance of the FindReplaceOptions class with the specified direction. |
| [FindReplaceOptions](./findreplaceoptions/)(Aspose::Words::Replacing::FindReplaceDirection, const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\> \&) | Initializes a new instance of the FindReplaceOptions class with the specified direction and replacing callback. |
| [FindReplaceOptions](./findreplaceoptions/)(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\> \&) | Initializes a new instance of the FindReplaceOptions class with the specified replacing callback. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| static [Type](./type/)() |  |
| [get_ApplyFont](./get_applyfont/)() const | Text formatting applied to new content. |
| [get_ApplyParagraphFormat](./get_applyparagraphformat/)() const | Paragraph formatting applied to new content. |
| [get_Direction](./get_direction/)() const | Selects direction for replace. Default value is [Forward](../findreplacedirection/). |
| [get_FindWholeWordsOnly](./get_findwholewordsonly/)() const | True indicates the oldValue must be a standalone word. |
| [get_IgnoreDeleted](./get_ignoredeleted/)() const | Gets or sets a boolean value indicating either to ignore text inside delete revisions. The default value is **false**. |
| [get_IgnoreFieldCodes](./get_ignorefieldcodes/)() const | Gets or sets a boolean value indicating either to ignore text inside field codes. The default value is **false**. |
| [get_IgnoreFields](./get_ignorefields/)() const | Gets or sets a boolean value indicating either to ignore text inside fields. The default value is **false**. |
| [get_IgnoreFootnotes](./get_ignorefootnotes/)() const | Gets or sets a boolean value indicating either to ignore footnotes. The default value is **false**. |
| [get_IgnoreInserted](./get_ignoreinserted/)() const | Gets or sets a boolean value indicating either to ignore text inside insert revisions. The default value is **false**. |
| [get_IgnoreOfficeMath](./get_ignoreofficemath/)() const | Gets or sets a boolean value indicating either to ignore text inside OfficeMath/>. The default value is **true**. |
| [get_IgnoreShapes](./get_ignoreshapes/)() const | Gets or sets a boolean value indicating either to ignore shapes within a text.

The default value is **false**. |
| [get_IgnoreStructuredDocumentTags](./get_ignorestructureddocumenttags/)() const | Gets or sets a boolean value indicating either to ignore content of [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/). The default value is **false**. |
| [get_LegacyMode](./get_legacymode/)() const | Gets or sets a boolean value indicating that old find/replace algorithm is used. |
| [get_MatchCase](./get_matchcase/)() const | True indicates case-sensitive comparison, false indicates case-insensitive comparison. |
| [get_ReplacementFormat](./get_replacementformat/)() const | Specifies format of the replacement. Default is [Text](../replacementformat/). |
| [get_ReplacingCallback](./get_replacingcallback/)() const | The user-defined method which is called before every replace occurrence. |
| [get_SmartParagraphBreakReplacement](./get_smartparagraphbreakreplacement/)() const | Gets or sets a boolean value indicating either it is allowed to replace paragraph break when there is no next sibling paragraph.

The default value is **false**. |
| [get_UseLegacyOrder](./get_uselegacyorder/)() const | True indicates that a text search is performed sequentially from top to bottom considering the text boxes. Default value is **false**. |
| [get_UseSubstitutions](./get_usesubstitutions/)() const | Gets or sets a boolean value indicating whether to recognize and use substitutions within replacement patterns. The default value is **false**. |
| [set_Direction](./set_direction/)(Aspose::Words::Replacing::FindReplaceDirection) | Selects direction for replace. Default value is [Forward](../findreplacedirection/). |
| [set_FindWholeWordsOnly](./set_findwholewordsonly/)(bool) | True indicates the oldValue must be a standalone word. |
| [set_IgnoreDeleted](./set_ignoredeleted/)(bool) | Sets a boolean value indicating either to ignore text inside delete revisions. The default value is **false**. |
| [set_IgnoreFieldCodes](./set_ignorefieldcodes/)(bool) | Sets a boolean value indicating either to ignore text inside field codes. The default value is **false**. |
| [set_IgnoreFields](./set_ignorefields/)(bool) | Sets a boolean value indicating either to ignore text inside fields. The default value is **false**. |
| [set_IgnoreFootnotes](./set_ignorefootnotes/)(bool) | Sets a boolean value indicating either to ignore footnotes. The default value is **false**. |
| [set_IgnoreInserted](./set_ignoreinserted/)(bool) | Sets a boolean value indicating either to ignore text inside insert revisions. The default value is **false**. |
| [set_IgnoreOfficeMath](./set_ignoreofficemath/)(bool) | Sets a boolean value indicating either to ignore text inside OfficeMath/>. The default value is **true**. |
| [set_IgnoreShapes](./set_ignoreshapes/)(bool) | Sets a boolean value indicating either to ignore shapes within a text.

The default value is **false**. |
| [set_IgnoreStructuredDocumentTags](./set_ignorestructureddocumenttags/)(bool) | Sets a boolean value indicating either to ignore content of [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/). The default value is **false**. |
| [set_LegacyMode](./set_legacymode/)(bool) | Sets a boolean value indicating that old find/replace algorithm is used. |
| [set_MatchCase](./set_matchcase/)(bool) | True indicates case-sensitive comparison, false indicates case-insensitive comparison. |
| [set_ReplacementFormat](./set_replacementformat/)(Aspose::Words::Replacing::ReplacementFormat) | Specifies format of the replacement. Default is [Text](../replacementformat/). |
| [set_ReplacingCallback](./set_replacingcallback/)(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\> \&) | The user-defined method which is called before every replace occurrence. |
| [set_SmartParagraphBreakReplacement](./set_smartparagraphbreakreplacement/)(bool) | Sets a boolean value indicating either it is allowed to replace paragraph break when there is no next sibling paragraph.

The default value is **false**. |
| [set_UseLegacyOrder](./set_uselegacyorder/)(bool) | True indicates that a text search is performed sequentially from top to bottom considering the text boxes. Default value is **false**. |
| [set_UseSubstitutions](./set_usesubstitutions/)(bool) | Sets a boolean value indicating whether to recognize and use substitutions within replacement patterns. The default value is **false**. |
## Examples


Shows how to toggle case sensitivity when performing a find-and-replace operation.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Set the "MatchCase" flag to "true" to apply case sensitivity while finding strings to replace.
// Set the "MatchCase" flag to "false" to ignore character case while searching for text to replace.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```

Shows how to toggle standalone word-only find-and-replace operations.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Set the "FindWholeWordsOnly" flag to "true" to replace the found text if it is not a part of another word.
// Set the "FindWholeWordsOnly" flag to "false" to replace all text regardless of its surroundings.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```
## See Also

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
