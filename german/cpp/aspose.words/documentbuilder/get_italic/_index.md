---
title: "Aspose::Words::DocumentBuilder::get_Italic-Methode"
linktitle: "get_Italic"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::get_Italic-Methode. Wahr, wenn die Schriftart in C++ als kursiv formatiert ist."
type: docs
weight: 21000
url: /de/cpp/aspose.words/documentbuilder/get_italic/
---
## DocumentBuilder::get_Italic method


True, wenn die Schrift als kursiv formatiert ist.

```cpp
bool Aspose::Words::DocumentBuilder::get_Italic()
```


## Beispiele



Zeigt, wie man MERGEFIELDs mit Daten mithilfe eines Document Builders anstelle eines Seriendrucks füllt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie einige MERGEFIELDS ein, die während eines Seriendrucks Daten aus Spalten mit demselben Namen in einer Datenquelle übernehmen,
// und füllen Sie sie anschließend manuell.
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

## Siehe auch

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
