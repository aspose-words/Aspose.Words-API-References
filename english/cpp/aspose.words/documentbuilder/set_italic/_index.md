---
title: Aspose::Words::DocumentBuilder::set_Italic method
linktitle: set_Italic
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::set_Italic method. True if the font is formatted as italic in C++.'
type: docs
weight: 94000
url: /cpp/aspose.words/documentbuilder/set_italic/
---
## DocumentBuilder::set_Italic method


True if the font is formatted as italic.

```cpp
void Aspose::Words::DocumentBuilder::set_Italic(bool value)
```

## Examples


Shows how to fill MERGEFIELDs with data with a document builder instead of a mail merge.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

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

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.FillMergeFields.docx");
```
## See Also

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
