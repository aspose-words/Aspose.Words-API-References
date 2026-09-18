---
title: "Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart Methode"
linktitle: "get_ContinuousSectionPageNumberingRestart"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart Methode. Ruft den Modus des Verhaltens zum Berechnen von Seitenzahlen ab oder legt ihn fest, wenn ein kontinuierlicher Abschnitt die Seitennummerierung neu startet, in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.layout/layoutoptions/get_continuoussectionpagenumberingrestart/
---
## LayoutOptions::get_ContinuousSectionPageNumberingRestart method


Liest oder schreibt den Verhaltensmodus zur Berechnung von Seitenzahlen, wenn ein fortlaufender Abschnitt die Seitennummerierung neu startet.

```cpp
Aspose::Words::Layout::ContinuousSectionRestart Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart() const
```


## Beispiele



Zeigt, wie man die Seitennummerierung in einem kontinuierlichen Abschnitt steuert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Continuous section page numbering.docx");

// Standardmäßig entspricht das Verhalten von Aspose.Words dem Microsoft Word 2019.
// Wenn Sie das alte Verhalten von Aspose.Words benötigen, wie in Microsoft Word 2016, verwenden Sie 'ContinuousSectionRestart.FromNewPageOnly'.
// Die Seitennummerierung wird nur neu gestartet, wenn vor dem Abschnitt auf der Seite, auf der der Abschnitt beginnt, kein anderer Inhalt vorhanden ist,
// dadurch wird die Nummerierung ab der zweiten Seite auf 2 zurückgesetzt.
doc->get_LayoutOptions()->set_ContinuousSectionPageNumberingRestart(Aspose::Words::Layout::ContinuousSectionRestart::FromNewPageOnly);
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Layout.RestartPageNumberingInContinuousSection.pdf");
```

## Siehe auch

* Enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
