---
title: get_SmartParagraphBreakReplacement
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a boolean value indicating either it is allowed to replace paragraph break when there is no next sibling paragraph. The default value is false.
type: docs
weight: 183
url: /cpp/aspose.words.replacing/findreplaceoptions/get_smartparagraphbreakreplacement/
---
## FindReplaceOptions.get_SmartParagraphBreakReplacement method


Gets or sets a boolean value indicating either it is allowed to replace paragraph break when there is no next sibling paragraph. The default value is **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement() const
```


## Examples




Shows how to remove paragraph from a table cell with a nested table. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Create table with paragraph and inner table in first cell.
builder->StartTable();
builder->InsertCell();
builder->Write(u"TEXT1");
builder->StartTable();
builder->InsertCell();
builder->EndTable();
builder->EndTable();
builder->Writeln();

auto options = MakeObject<FindReplaceOptions>();
// When the following option is set to 'true', Aspose.Words will remove paragraph's text
// completely with its paragraph mark. Otherwise, Aspose.Words will mimic Word and remove
// only paragraph's text and leaves the paragraph mark intact (when a table follows the text).
options->set_SmartParagraphBreakReplacement(isSmartParagraphBreakReplacement);
doc->get_Range()->Replace(MakeObject<System::Text::RegularExpressions::Regex>(u"TEXT1&p"), u"", options);

doc->Save(ArtifactsDir + u"Table.RemoveParagraphTextAndMark.docx");
```

