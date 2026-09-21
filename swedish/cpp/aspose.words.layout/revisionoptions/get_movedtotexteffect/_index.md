---
title: "Aspose::Words::Layout::RevisionOptions::get_MovedToTextEffect metod"
linktitle: "get_MovedToTextEffect"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Layout::RevisionOptions::get_MovedToTextEffect metod. Tillåter att ange effekten som ska tillämpas på de områden där innehållet flyttades till Moving. Standardvärdet är DoubleUnderline i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words.layout/revisionoptions/get_movedtotexteffect/
---
## RevisionOptions::get_MovedToTextEffect method


Tillåter att ange effekten som ska tillämpas på de områden där innehållet flyttades till [Moving](../../../aspose.words/revisiontype/). Standardvärdet är [DoubleUnderline](../../revisiontexteffect/)

```cpp
Aspose::Words::Layout::RevisionTextEffect Aspose::Words::Layout::RevisionOptions::get_MovedToTextEffect()
```


## Exempel



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

* Enum [RevisionTextEffect](../../revisiontexteffect/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
