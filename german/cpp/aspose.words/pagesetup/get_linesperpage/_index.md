---
title: "Aspose::Words::PageSetup::get_LinesPerPage-Methode"
linktitle: "get_LinesPerPage"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageSetup::get_LinesPerPage-Methode. Gibt die Anzahl der Zeilen pro Seite im Dokumentgitter zurück oder legt sie fest in C++."
type: docs
weight: 26000
url: /de/cpp/aspose.words/pagesetup/get_linesperpage/
---
## PageSetup::get_LinesPerPage method


Liest oder legt die Anzahl der Zeilen pro Seite im Dokumentengitter fest.

```cpp
int32_t Aspose::Words::PageSetup::get_LinesPerPage()
```

## Hinweise


Der Minimalwert der Eigenschaft ist 1. Der Maximalwert hängt von der Seitenhöhe und der Schriftgröße des Normal-Stils ab. Der minimale Zeilenabstand beträgt 136 Prozent der Schriftgröße. Zum Beispiel beträgt die maximale Zeilenanzahl pro Seite einer Letter-Seite mit ein‑Zoll‑Rändern 39.

Standardmäßig hat die Eigenschaft einen Wert, bei dem der Zeilenabstand das 1,5‑fache der Schriftgröße des Normal-Stils beträgt.

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

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
