---
title: "Aspose::Words::Layout::RevisionColor enum"
linktitle: "RevisionColor"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Layout::RevisionColor enum. Tillåter att ange färg på dokumentrevisioner i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words.layout/revisioncolor/
---
## RevisionColor enum


Tillåter att ange färg för dokumentrevisioner.

```cpp
enum class RevisionColor
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Auto | 0 | Standard. |
| Svart | 1 | Representerar färgen 000000. |
| Blå | 2 | Representerar färgen 2e97d3. |
| Ljusgrön | 3 | Representerar färgen 84a35b. |
| ClassicBlue | 4 | Representerar färgen 0000ff. |
| ClassicRed | 5 | Representerar färgen ff0000. |
| DarkBlue | 6 | Representerar färgen 376e96. |
| DarkRed | 7 | Representerar färgen 881824. |
| Mörkgul | 8 | Representerar färgen e09a2b. |
| Grå25 | 9 | Representerar färgen a0a3a9. |
| Grå50 | 10 | Representerar färgen 50565e. |
| Grön | 11 | Representerar färgen 2c6234. |
| Rosa | 12 | Representerar färgen ce338f. |
| Röd | 13 | Representerar färgen b5082e. |
| Blågrön | 14 | Representerar färgen 1b9cab. |
| Turkos | 15 | Representerar färgen 3eafc2. |
| Violett | 16 | Representerar färgen 633277. |
| Vit | 17 | Representerar färgen ffffff. |
| Gul | 18 | Representerar färgen fad272. |
| Ljusrosa | 19 | Representerar färgen fce6f4. |
| Ljusblå | 20 | Representerar färgen e1f2fa. |
| Ljusgul | 21 | Representerar färgen fef4de. |
| Ljuslila | 22 | Representerar färgen eadfef. |
| Ljusorange | 23 | Representerar färgen fce3d0. |
| Ljusgrön | 24 | Representerar färgen e9f8ce. |
| Grå | 25 | Representerar färgen efeded. |
| IngenMarkering | 26 | Ingen färg används för att markera revisionsändringar. |
| EfterFörfattare | 27 | Revisioner av varje författare får sin egen färg för markering från en fördefinierad uppsättning högkontrastfärger. |


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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
