---
title: "Aspose::Words::Layout::ContinuousSectionRestart enum"
linktitle: "ContinuousSectionRestart"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Layout::ContinuousSectionRestart enum. Stellt verschiedene Verhaltensweisen dar, wenn Seitenzahlen in einem kontinuierlichen Abschnitt berechnet werden, der die Seitennummerierung in C++ neu startet."
type: docs
weight: 8000
url: /de/cpp/aspose.words.layout/continuoussectionrestart/
---
## ContinuousSectionRestart enum


Stellt verschiedene Verhaltensweisen beim Berechnen von Seitenzahlen in einem fortlaufenden Abschnitt dar, der die Seitennummerierung neu startet.

```cpp
enum class ContinuousSectionRestart
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Immer | 0 | Die Seitennummerierung wird immer neu gestartet, unabhängig vom Inhaltsfluss. |
| FromNewPageOnly | 1 | Die Seitennummerierung wird nur neu gestartet, wenn vor dem Abschnitt auf der Seite, auf der der Abschnitt beginnt, kein anderer Inhalt vorhanden ist. |


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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
