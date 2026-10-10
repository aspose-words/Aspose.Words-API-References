---
title: "Aspose::Words::DocumentBuilder::get_Italic metod"
linktitle: "get_Italic"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::get_Italic metod. Sant om teckensnittet är formaterat som kursiv i C++."
type: docs
weight: 21000
url: /sv/cpp/aspose.words/documentbuilder/get_italic/
---
## DocumentBuilder::get_Italic method


Sant om teckensnittet är formaterat som kursiv.

```cpp
bool Aspose::Words::DocumentBuilder::get_Italic()
```


## Exempel



Visar hur man fyller MERGEFIELDs med data med en dokumentbyggare istället för en mail merge.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga några MERGEFIELDS, som accepterar data från kolumner med samma namn i en datakälla under en mail merge,
// och fyll sedan i dem manuellt.
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

## Se även

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
