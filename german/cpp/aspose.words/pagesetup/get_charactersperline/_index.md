---
title: "Aspose::Words::PageSetup::get_CharactersPerLine Methode"
linktitle: "get_CharactersPerLine"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageSetup::get_CharactersPerLine Methode. Liest oder setzt die Anzahl der Zeichen pro Zeile im Dokumentgitter in C++."
type: docs
weight: 12000
url: /de/cpp/aspose.words/pagesetup/get_charactersperline/
---
## PageSetup::get_CharactersPerLine method


Liest oder legt die Anzahl der Zeichen pro Zeile im Dokumentengitter fest.

```cpp
int32_t Aspose::Words::PageSetup::get_CharactersPerLine()
```

## Hinweise


Der Minimalwert der Eigenschaft ist 1. Der Maximalwert hängt von der Seitenbreite und der Schriftgröße des Normal-Stils ab. Der minimale Zeichenabstand beträgt 90 Prozent der Schriftgröße. Zum Beispiel beträgt die maximale Anzahl von Zeichen pro Zeile einer Letter-Seite mit ein‑Zoll‑Rändern 43.

Standardmäßig hat die Eigenschaft einen Wert, bei dem die Zeichenbreite der Schriftgröße des Normalstils entspricht.

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

## Siehe auch

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
