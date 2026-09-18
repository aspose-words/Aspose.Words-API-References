---
title: "Aspose::Words::ParagraphFormat::get_SnapToGrid‑Methode"
linktitle: "get_SnapToGrid"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphFormat::get_SnapToGrid‑Methode. Gibt an, ob der aktuelle Absatz die Dokument‑Rasterlinien‑Einstellungen pro Seite beim Layouten des Inhalts im Absatz in C++ verwenden soll."
type: docs
weight: 30000
url: /de/cpp/aspose.words/paragraphformat/get_snaptogrid/
---
## ParagraphFormat::get_SnapToGrid method


Gibt an, ob der aktuelle Absatz die Dokumentgitterlinien‑pro‑Seite‑Einstellungen beim Layouten des Inhalts im Absatz verwenden soll.

```cpp
bool Aspose::Words::ParagraphFormat::get_SnapToGrid()
```


## Beispiele



Zeigt, wie man ein Limit für die Anzahl der Zeilen, die jede Seite haben darf, festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aktivieren Sie das Pitching und verwenden Sie es anschließend, um die Anzahl der Zeilen pro Seite in diesem Abschnitt festzulegen.
// Eine ausreichend große Schriftgröße schiebt einige Zeilen auf die nächste Seite, um überlappende Zeichen zu vermeiden.
builder->get_PageSetup()->set_LayoutMode(Aspose::Words::SectionLayoutMode::LineGrid);
builder->get_PageSetup()->set_LinesPerPage(15);

builder->get_ParagraphFormat()->set_SnapToGrid(true);

for (int32_t i = 0; i < 30; i++)
{
    builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
}

doc->Save(get_ArtifactsDir() + u"PageSetup.LinesPerPage.docx");
```

## Siehe auch

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
