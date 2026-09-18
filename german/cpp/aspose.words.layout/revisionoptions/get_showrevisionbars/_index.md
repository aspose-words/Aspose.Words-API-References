---
title: "Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars Methode"
linktitle: "get_ShowRevisionBars"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars Methode. Ermöglicht die Angabe, ob Revisionsbalken in der Nähe von Zeilen mit überarbeitetem Inhalt angezeigt werden sollen. Der Standardwert ist true in C++."
type: docs
weight: 19000
url: /de/cpp/aspose.words.layout/revisionoptions/get_showrevisionbars/
---
## RevisionOptions::get_ShowRevisionBars method


Ermöglicht die Angabe, ob Revisionsbalken in der Nähe von Zeilen mit überarbeitetem Inhalt dargestellt werden sollen. Der Standardwert ist **true**.

```cpp
bool Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars() const
```


## Beispiele



Zeigt, wie man das Aussehen von Revisionen in einem gerenderten Ausgabedokument ändert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie eine Revision ein und ändern Sie dann die Farbe aller Revisionen zu Grün.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Entfernen Sie die Leiste, die links von jeder überarbeiteten Zeile erscheint.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## Siehe auch

* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
