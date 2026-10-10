---
title: "Aspose::Words::SectionLayoutMode Enum"
linktitle: "SectionLayoutMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::SectionLayoutMode Enum. Gibt den Layoutmodus für einen Abschnitt an, der es ermöglicht, das Verhalten des Dokumentengitters in C++ zu definieren."
type: docs
weight: 115000
url: /de/cpp/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enum


Gibt den Layoutmodus für einen Abschnitt an, der die Definition des Dokumentgitterverhaltens ermöglicht.

```cpp
enum class SectionLayoutMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Standard | 0 | Gibt an, dass kein Dokumentengitter auf den Inhalt des entsprechenden Abschnitts im Dokument angewendet wird. |
| Gitter | 1 | Gibt an, dass der entsprechende Abschnitt sowohl die zusätzliche Zeilenhöhe als auch die Zeichenhöhe zu jeder Zeile und jedem Zeichen innerhalb des Abschnitts hinzufügt, um eine bestimmte Anzahl von Zeilen pro Seite und Zeichen pro Zeile beizubehalten. Zeichen werden beim Tippen nicht automatisch an den Gitterlinien ausgerichtet. |
| LineGrid | 2 | Gibt an, dass dem entsprechenden Abschnitt eine zusätzliche Zeilenhöhe zu jeder Zeile innerhalb des Abschnitts hinzugefügt wird, um die festgelegte Anzahl von Zeilen pro Seite beizubehalten. |
| SnapToChars | 3 | Gibt an, dass der entsprechende Abschnitt sowohl den zusätzlichen Zeilenabstand als auch den Zeichenabstand zu jeder Zeile und jedem Zeichen innerhalb des Abschnitts hinzufügt, um eine bestimmte Anzahl von Zeilen pro Seite und Zeichen pro Zeile beizubehalten. Zeichen werden beim Tippen automatisch an den Rasterlinien ausgerichtet. |


## Beispiele



Zeigt, wie man die Anzahl der Zeichen, die jede Zeile haben darf, angibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aktivieren Sie das Pitching und verwenden Sie es anschließend, um die Anzahl der Zeichen pro Zeile in diesem Abschnitt festzulegen.
builder->get_PageSetup()->set_LayoutMode(Aspose::Words::SectionLayoutMode::Grid);
builder->get_PageSetup()->set_CharactersPerLine(10);

// Die Anzahl der Zeichen hängt ebenfalls von der Schriftgröße ab.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(20);

ASSERT_EQ(8, doc->get_FirstSection()->get_PageSetup()->get_CharactersPerLine());

builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CharactersPerLine.docx");
```


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
