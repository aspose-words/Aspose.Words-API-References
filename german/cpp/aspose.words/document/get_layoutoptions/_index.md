---
title: "Aspose::Words::Document::get_LayoutOptions Methode"
linktitle: "get_LayoutOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_LayoutOptions Methode. Gibt ein LayoutOptions-Objekt zurück, das Optionen zur Steuerung des Layout‑Prozesses dieses Dokuments in C++ darstellt."
type: docs
weight: 36000
url: /de/cpp/aspose.words/document/get_layoutoptions/
---
## Document::get_LayoutOptions method


Gibt ein [LayoutOptions](../../../aspose.words.layout/layoutoptions/) Objekt zurück, das Optionen zur Steuerung des Layout‑Prozesses dieses Dokuments darstellt.

```cpp
System::SharedPtr<Aspose::Words::Layout::LayoutOptions> Aspose::Words::Document::get_LayoutOptions() const
```


## Beispiele



Zeigt, wie man Text in einem gerenderten Ausgabedokument ausblendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie versteckten Text ein und geben Sie dann an, ob wir ihn aus einem gerenderten Dokument weglassen möchten.
builder->Writeln(u"This text is not hidden.");
builder->get_Font()->set_Hidden(true);
builder->Writeln(u"This text is hidden.");

doc->get_LayoutOptions()->set_ShowHiddenText(showHiddenText);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsHiddenText.pdf");
```


Zeigt, wie man Absatzmarken in einem gerenderten Ausgabedokument anzeigt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie einige Absätze hinzu und aktivieren Sie dann Absatzmarken, um das Ende der Absätze anzuzeigen
// mit einem Pilcrow‑Symbol (¶), wenn wir das Dokument rendern.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

doc->get_LayoutOptions()->set_ShowParagraphMarks(showParagraphMarks);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsParagraphMarks.pdf");
```


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

* Class [LayoutOptions](../../../aspose.words.layout/layoutoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
