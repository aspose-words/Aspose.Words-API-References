---
title: "Aspose::Words::TabStopCollection::After-Methode"
linktitle: "Nach"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TabStopCollection::After-Methode. Gibt den ersten Tabstopp rechts von der angegebenen Position in C++ zurück."
type: docs
weight: 3000
url: /de/cpp/aspose.words/tabstopcollection/after/
---
## TabStopCollection::After method


Gibt den ersten Tabulator rechts von der angegebenen Position zurück.

```cpp
System::SharedPtr<Aspose::Words::TabStop> Aspose::Words::TabStopCollection::After(double position)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Position | double | Die Referenzposition (in Punkten). |

### ReturnValue

Ein Tabstopp-Objekt oder **null**, wenn kein geeigneter Tabstopp gefunden wurde.
## Hinweise


Überspringt Tabstopps mit [Alignment](../../tabstop/get_alignment/) auf [Bar](../../tabalignment/) gesetzt.

## Beispiele



Zeigt, wie man mit der Tabulatorsammlung eines Dokuments arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = builder->get_ParagraphFormat()->get_TabStops();

// 72 Punkte entsprechen einem "Zoll" auf der Tabulatorlineal von Microsoft Word.
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(72.0));
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(432.0, Aspose::Words::TabAlignment::Right, Aspose::Words::TabLeader::Dashes));

ASSERT_EQ(2, tabStops->get_Count());
ASSERT_FALSE(tabStops->idx_get(0)->get_IsClear());
ASSERT_FALSE(System::ObjectExt::Equals(tabStops->idx_get(0), tabStops->idx_get(1)));

// Jedes "Tab"‑Zeichen bewegt den Cursor des Builders zur Position des nächsten Tabulators.
builder->Writeln(u"Start\tTab 1\tTab 2");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(2, paragraphs->get_Count());

// Jeder Absatz erhält seine Tabulatorsammlung, die ihre Werte aus der Tabulatorsammlung des Dokument‑Builders kopiert.
ASPOSE_ASSERT_EQ(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());
ASPOSE_ASSERT_NS(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());

// Eine Tabstoppsammlung kann uns zu TabStops vor und nach bestimmten Positionen führen.
ASPOSE_ASSERT_EQ(72.0, tabStops->Before(100.0)->get_Position());
ASPOSE_ASSERT_EQ(432.0, tabStops->After(100.0)->get_Position());

// Wir können die Tabstoppsammlung eines Absatzes löschen, um zum Standard-Tab-Verhalten zurückzukehren.
paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->Clear();

ASSERT_EQ(0, paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->get_Count());

doc->Save(get_ArtifactsDir() + u"TabStopCollection.TabStopCollection.docx");
```

## Siehe auch

* Class [TabStop](../../tabstop/)
* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
