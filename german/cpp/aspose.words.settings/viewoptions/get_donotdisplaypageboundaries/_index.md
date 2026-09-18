---
title: "Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries-Methode"
linktitle: "get_DoNotDisplayPageBoundaries"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries-Methode. Deaktiviert die Anzeige des Abstands zwischen dem oberen Rand des Textes und dem oberen Seitenrand in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.settings/viewoptions/get_donotdisplaypageboundaries/
---
## ViewOptions::get_DoNotDisplayPageBoundaries method


Schaltet die Anzeige des Abstands zwischen dem oberen Rand des Textes und dem oberen Rand der Seite aus.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries() const
```


## Beispiele



Zeigt, wie man vertikalen Leerraum sowie Kopf‑ und Fußzeilen in den Ansichtseinstellungen ausblendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie Inhalt ein, der sich über 3 Seiten erstreckt.
builder->Writeln(u"Paragraph 1, Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Paragraph 2, Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Paragraph 3, Page 3.");

// Fügen Sie eine Kopfzeile und eine Fußzeile ein.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"This is the header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"This is the footer.");

// Dieses Dokument enthält eine kleine Menge an Inhalt, die jedoch einige ganze Seiten Platz einnimmt.
// Setzen Sie das Flag "DoNotDisplayPageBoundaries" auf "true", um ältere Versionen von Microsoft Word dazu zu bringen, Kopfzeilen zu unterdrücken,
// Fußzeilen und einen Großteil des vertikalen Leerraums beim Anzeigen unseres Dokuments zu entfernen.
// Setzen Sie das Flag "DoNotDisplayPageBoundaries" auf "false", um ältere Versionen von Microsoft Word zu erhalten
// um unser Dokument normal anzuzeigen.
doc->get_ViewOptions()->set_DoNotDisplayPageBoundaries(doNotDisplayPageBoundaries);

doc->Save(get_ArtifactsDir() + u"ViewOptions.DisplayPageBoundaries.doc");
```

## Siehe auch

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
