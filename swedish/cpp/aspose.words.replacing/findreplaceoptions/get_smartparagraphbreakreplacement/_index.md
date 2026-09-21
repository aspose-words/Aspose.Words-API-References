---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement method"
linktitle: "get_SmartParagraphBreakReplacement"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement method. Hämtar eller anger ett booleskt värde som indikerar om det är tillåtet att ersätta styckebrytning när det inte finns något nästa syskonstycke. Standardvärdet är false i C++."
type: docs
weight: 16000
url: /sv/cpp/aspose.words.replacing/findreplaceoptions/get_smartparagraphbreakreplacement/
---
## FindReplaceOptions::get_SmartParagraphBreakReplacement method


Hämtar eller anger ett booleskt värde som indikerar om det är tillåtet att ersätta styckeavbrott när det inte finns något nästa syskonstycke. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement() const
```


## Exempel



Visar hur man tar bort ett stycke från en tabellcell med en inbäddad tabell.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skapa en tabell med stycke och inre tabell i den första cellen.
builder->StartTable();
builder->InsertCell();
builder->Write(u"TEXT1");
builder->StartTable();
builder->InsertCell();
builder->EndTable();
builder->EndTable();
builder->Writeln();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
// När följande alternativ är satt till 'true' kommer Aspose.Words att ta bort styckets text
// fullständigt tillsammans med dess stycketecken. Annars kommer Aspose.Words att efterlikna Word och ta bort
// endast styckets text och lämnar styckesmärket intakt (när en tabell följer texten).
options->set_SmartParagraphBreakReplacement(isSmartParagraphBreakReplacement);
doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"TEXT1&p"), u"", options);

doc->Save(get_ArtifactsDir() + u"Table.RemoveParagraphTextAndMark.docx");
```

## Se även

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
