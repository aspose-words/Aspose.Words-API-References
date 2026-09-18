---
title: "Aspose::Words::TabAlignment enum"
linktitle: "TabAlignment"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TabAlignment enum. Gibt die Ausrichtung/Art eines Tabstopps in C++ an."
type: docs
weight: 120000
url: /de/cpp/aspose.words/tabalignment/
---
## TabAlignment enum


Gibt die Ausrichtung/den Typ eines Tabstopp an.

```cpp
enum class TabAlignment
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Links | 0 | Richtet den Text nach dem Tabstopp linksbündig aus. |
| Mitte | 1 | Zentriert den Text um den Tabstopp. |
| Rechts | 2 | Richtet den Text am Tabstopp rechtsbündig aus. |
| Decimal | 3 | Richtet den Text am Dezimalpunkt aus. |
| Bar | 4 | Zeichnet einen vertikalen Balken an der Position des Tabstopps. |
| Liste | 6 | Der Tab ist ein Trennzeichen zwischen Nummer/Aufzählungszeichen und Text in einem Listeneintrag. |
| Clear | 7 | Löscht jeden Tabstopp an dieser Position. |


## Beispiele



Zeigt, wie benutzerdefinierte Tabstopps für einen Absatz festgelegt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Wenn wir uns in einem Absatz ohne Tabstopps in dieser Sammlung befinden,
// springt der Cursor jedes Mal um 36 Punkte, wenn wir die Tabulatortaste in Microsoft Word drücken.
ASSERT_EQ(0, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetEffectiveTabStops()->get_Length());

// Wir können benutzerdefinierte Tabstopps in Microsoft Word hinzufügen, wenn wir das Lineal über die Registerkarte "View" aktivieren.
// Jede Einheit auf diesem Lineal entspricht zwei Standard-Tabstopps, also 72 Punkte.
// Wir können benutzerdefinierte Tabstopps programmgesteuert wie folgt hinzufügen.
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_TabStops();
tabStops->Add(72, Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dots);
tabStops->Add(216, Aspose::Words::TabAlignment::Center, Aspose::Words::TabLeader::Dashes);
tabStops->Add(360, Aspose::Words::TabAlignment::Right, Aspose::Words::TabLeader::Line);

// Wir können diese Tabstopps in Microsoft Word sehen, indem wir das Lineal über "View" -> "Show" -> "Ruler" aktivieren.
ASSERT_EQ(3, para->GetEffectiveTabStops()->get_Length());

// Alle Tabulatorzeichen, die wir hinzufügen, nutzen die Tabstopps auf dem Lineal und können,
// Je nach Wert des Tab‑Leaders eine Zeile zwischen den Tab‑Abgangs- und Ankunftszielen einfügen.
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"\tTab 1\tTab 2\tTab 3"));

doc->Save(get_ArtifactsDir() + u"Paragraph.TabStops.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
