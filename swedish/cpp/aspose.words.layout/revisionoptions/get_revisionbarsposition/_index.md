---
title: "Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition metod"
linktitle: "get_RevisionBarsPosition"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition metod. Hämtar eller anger renderingsposition för revisionsstaplar. Standardvärdet är Outside i C++."
type: docs
weight: 15000
url: /sv/cpp/aspose.words.layout/revisionoptions/get_revisionbarsposition/
---
## RevisionOptions::get_RevisionBarsPosition method


Hämtar eller anger renderingsposition för revisionsstaplar. Standardvärdet är [Outside](../../../aspose.words.drawing/horizontalalignment/).

```cpp
Aspose::Words::Drawing::HorizontalAlignment Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition() const
```


## Exempel



Visar hur man ändrar utseendet på revisioner i ett renderat utdata-dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en revision och ändra sedan färgen på alla revisioner till grön.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Ta bort stapeln som visas till vänster om varje reviderad rad.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## Se även

* Enum [HorizontalAlignment](../../../aspose.words.drawing/horizontalalignment/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
