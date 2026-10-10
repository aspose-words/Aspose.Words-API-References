---
title: "Aspose::Words::Layout::RevisionOptions::get_ShowInBalloons metod"
linktitle: "get_ShowInBalloons"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Layout::RevisionOptions::get_ShowInBalloons metod. Tillåter att ange om revisionerna renderas i ballonger. Standardvärdet är None i C++."
type: docs
weight: 17000
url: /sv/cpp/aspose.words.layout/revisionoptions/get_showinballoons/
---
## RevisionOptions::get_ShowInBalloons method


Tillåter att ange om revisionerna renderas i ballonger. Standardvärdet är [None](../../showinballoons/).

```cpp
Aspose::Words::Layout::ShowInBalloons Aspose::Words::Layout::RevisionOptions::get_ShowInBalloons() const
```


## Exempel



Visar hur man visar revisioner i ballonger.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

// Som standard har text som är en revision en annan färg för att särskilja den från annan icke-revisions‑text.
// Ställ in ett revisionsalternativ för att visa fler detaljer om varje revision i en ballong på sidans högra marginal.
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowInBalloons(Aspose::Words::Layout::ShowInBalloons::FormatAndDelete);
doc->Save(get_ArtifactsDir() + u"Revision.ShowRevisionBalloons.pdf");
```


Visar hur man ändrar utseendet på revisioner.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

// Hämta RevisionOptions‑objektet som styr utseendet på revisioner.
System::SharedPtr<Aspose::Words::Layout::RevisionOptions> revisionOptions = doc->get_LayoutOptions()->get_RevisionOptions();

// Rendera insättningsrevisioner i grönt och kursivt.
revisionOptions->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::Green);
revisionOptions->set_InsertedTextEffect(Aspose::Words::Layout::RevisionTextEffect::Italic);

// Rendera raderingsrevisioner i rött och fetstil.
revisionOptions->set_DeletedTextColor(Aspose::Words::Layout::RevisionColor::Red);
revisionOptions->set_DeletedTextEffect(Aspose::Words::Layout::RevisionTextEffect::Bold);

// Samma text kommer att visas två gånger i en flyttningsrevision:
// en gång vid avresepunkten och en gång vid ankomstdestinationen.
// Rendera texten vid den flyttade‑från‑revisionen gul med dubbelt genomstrykning
// och dubbelt understruket blått vid den flyttade‑till‑revisionen.
revisionOptions->set_MovedFromTextColor(Aspose::Words::Layout::RevisionColor::Yellow);
revisionOptions->set_MovedFromTextEffect(Aspose::Words::Layout::RevisionTextEffect::DoubleStrikeThrough);
revisionOptions->set_MovedToTextColor(Aspose::Words::Layout::RevisionColor::ClassicBlue);
revisionOptions->set_MovedToTextEffect(Aspose::Words::Layout::RevisionTextEffect::DoubleUnderline);

// Rendera formatrevisioner i mörkrött och fetstil.
revisionOptions->set_RevisedPropertiesColor(Aspose::Words::Layout::RevisionColor::DarkRed);
revisionOptions->set_RevisedPropertiesEffect(Aspose::Words::Layout::RevisionTextEffect::Bold);

// Placera ett tjockt mörkblått streck på sidans vänstra sida bredvid rader som påverkats av revisioner.
revisionOptions->set_RevisionBarsColor(Aspose::Words::Layout::RevisionColor::DarkBlue);
revisionOptions->set_RevisionBarsWidth(15.0f);

// Visa revisionsmarkeringar och originaltext.
revisionOptions->set_ShowOriginalRevision(true);
revisionOptions->set_ShowRevisionMarks(true);

// Få rörelse, borttagning, formateringsrevisioner och kommentarer att visas i gröna ballonger
// på högra sidan av sidan.
revisionOptions->set_ShowInBalloons(Aspose::Words::Layout::ShowInBalloons::Format);
revisionOptions->set_CommentColor(Aspose::Words::Layout::RevisionColor::BrightGreen);

// Dessa funktioner gäller endast för format som .pdf eller .jpg.
doc->Save(get_ArtifactsDir() + u"Revision.RevisionOptions.pdf");
```

## Se även

* Enum [ShowInBalloons](../../showinballoons/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
