---
title: get_Italic
second_title: Aspose.Words for C++ API Reference
description: True if the font is formatted as italic.
type: docs
weight: 248
url: /cpp/aspose.words/documentbuilder/get_italic/
---
## DocumentBuilder.get_Italic method


True if the font is formatted as italic.

```cpp
bool Aspose::Words::DocumentBuilder::get_Italic()
```


## Examples




Shows how to fill MERGEFIELDs with data with a document builder instead of a mail merge. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
// and then fill them manually.
builder->InsertField(u" MERGEFIELD Chairman ");
builder->InsertField(u" MERGEFIELD ChiefFinancialOfficer ");
builder->InsertField(u" MERGEFIELD ChiefTechnologyOfficer ");

builder->MoveToMergeField(u"Chairman");
builder->set_Bold(true);
builder->Writeln(u"John Doe");

builder->MoveToMergeField(u"ChiefFinancialOfficer");
builder->set_Italic(true);
builder->Writeln(u"Jane Doe");

builder->MoveToMergeField(u"ChiefTechnologyOfficer");
builder->set_Italic(true);
builder->Writeln(u"John Bloggs");

doc->Save(ArtifactsDir + u"DocumentBuilder.FillMergeFields.docx");
```

