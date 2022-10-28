---
title: FindReplaceOptions
second_title: Aspose.Words for C++ API Reference
description: Specifies options for find/replace operations.
type: docs
weight: 1
url: /cpp/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class


Specifies options for find/replace operations.

```cpp
class FindReplaceOptions : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [FindReplaceOptions](./findreplaceoptions/)() |  |
| [FindReplaceOptions](./findreplaceoptions/)(Aspose::Words::Replacing::FindReplaceDirection) |  |
| [FindReplaceOptions](./findreplaceoptions/)(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) |  |
| [FindReplaceOptions](./findreplaceoptions/)(Aspose::Words::Replacing::FindReplaceDirection, const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) |  |
| [get_ApplyFont](./get_applyfont/)() const | Text formatting applied to new content. |
| [get_ApplyParagraphFormat](./get_applyparagraphformat/)() const | [Paragraph](../../aspose.words/paragraph/) formatting applied to new content. |
| [get_Direction](./get_direction/)() const | Selects direction for replace. Default value is **Forward**. |
| [get_FindWholeWordsOnly](./get_findwholewordsonly/)() const | True indicates the oldValue must be a standalone word. |
| [get_IgnoreDeleted](./get_ignoredeleted/)() const | Gets or sets a boolean value indicating either to ignore text inside delete revisions. The default value is **false**. |
| [get_IgnoreFieldCodes](./get_ignorefieldcodes/)() const | Gets or sets a boolean value indicating either to ignore text inside field codes. The default value is **false**. |
| [get_IgnoreFields](./get_ignorefields/)() const | Gets or sets a boolean value indicating either to ignore text inside fields. The default value is **false**. |
| [get_IgnoreFootnotes](./get_ignorefootnotes/)() const | Gets or sets a boolean value indicating either to ignore footnotes. The default value is **false**. |
| [get_IgnoreInserted](./get_ignoreinserted/)() const | Gets or sets a boolean value indicating either to ignore text inside insert revisions. The default value is **false**. |
| [get_IgnoreStructuredDocumentTags](./get_ignorestructureddocumenttags/)() const | Gets or sets a boolean value indicating either to ignore content of [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/). The default value is **false**. |
| [get_LegacyMode](./get_legacymode/)() const | Gets or sets a boolean value indicating that old find/replace algorithm is used. |
| [get_MatchCase](./get_matchcase/)() const | True indicates case-sensitive comparison, false indicates case-insensitive comparison. |
| [get_ReplacingCallback](./get_replacingcallback/)() const | The user-defined method which is called before every replace occurrence. |
| [get_SmartParagraphBreakReplacement](./get_smartparagraphbreakreplacement/)() const | Gets or sets a boolean value indicating either it is allowed to replace paragraph break when there is no next sibling paragraph. The default value is **false**. |
| [get_UseLegacyOrder](./get_uselegacyorder/)() const | True indicates that a text search is performed sequentially from top to bottom considering the text boxes. Default value is false. |
| [get_UseSubstitutions](./get_usesubstitutions/)() const | Gets or sets a boolean value indicating whether to recognize and use substitutions within replacement patterns. The default value is **false**. |
| [set_Direction](./set_direction/)(Aspose::Words::Replacing::FindReplaceDirection) | Setter for [Aspose::Words::Replacing::FindReplaceOptions::get_Direction](./get_direction/). |
| [set_FindWholeWordsOnly](./set_findwholewordsonly/)(bool) | Setter for [Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly](./get_findwholewordsonly/). |
| [set_IgnoreDeleted](./set_ignoredeleted/)(bool) | Setter for [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted](./get_ignoredeleted/). |
| [set_IgnoreFieldCodes](./set_ignorefieldcodes/)(bool) | Setter for [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes](./get_ignorefieldcodes/). |
| [set_IgnoreFields](./set_ignorefields/)(bool) | Setter for [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields](./get_ignorefields/). |
| [set_IgnoreFootnotes](./set_ignorefootnotes/)(bool) | Setter for [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes](./get_ignorefootnotes/). |
| [set_IgnoreInserted](./set_ignoreinserted/)(bool) | Setter for [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted](./get_ignoreinserted/). |
| [set_IgnoreStructuredDocumentTags](./set_ignorestructureddocumenttags/)(bool) | Setter for [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags](./get_ignorestructureddocumenttags/). |
| [set_LegacyMode](./set_legacymode/)(bool) | Setter for [Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode](./get_legacymode/). |
| [set_MatchCase](./set_matchcase/)(bool) | Setter for [Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase](./get_matchcase/). |
| [set_ReplacingCallback](./set_replacingcallback/)(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | Setter for [Aspose::Words::Replacing::FindReplaceOptions::get_ReplacingCallback](./get_replacingcallback/). |
| [set_SmartParagraphBreakReplacement](./set_smartparagraphbreakreplacement/)(bool) | Setter for [Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement](./get_smartparagraphbreakreplacement/). |
| [set_UseLegacyOrder](./set_uselegacyorder/)(bool) | Setter for [Aspose::Words::Replacing::FindReplaceOptions::get_UseLegacyOrder](./get_uselegacyorder/). |
| [set_UseSubstitutions](./set_usesubstitutions/)(bool) | Setter for [Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions](./get_usesubstitutions/). |

## Examples




Shows how to toggle case sensitivity when performing a find-and-replace operation. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
auto options = MakeObject<FindReplaceOptions>();

// Set the "MatchCase" flag to "true" to apply case sensitivity while finding strings to replace.
// Set the "MatchCase" flag to "false" to ignore character case while searching for text to replace.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? String(u"Jade bought a ruby necklace.") : String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```


Shows how to toggle standalone word-only find-and-replace operations. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
auto options = MakeObject<FindReplaceOptions>();

// Set the "FindWholeWordsOnly" flag to "true" to replace the found text if it is not a part of another word.
// Set the "FindWholeWordsOnly" flag to "false" to replace all text regardless of its surroundings.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? String(u"Louis will meet you in Jacksonville.") : String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```

