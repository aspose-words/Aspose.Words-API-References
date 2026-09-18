---
title: "Aspose::Words::Paragraph::GetEffectiveTabStops method"
linktitle: "GetEffectiveTabStops"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Paragraph::GetEffectiveTabStops method. Gibt ein Array aller Tabstopps zurück, die auf diesen Absatz angewendet wurden, einschließlich der indirekt durch Stile oder Listen in C++ angewendeten."
type: docs
weight: 26000
url: /de/cpp/aspose.words/paragraph/geteffectivetabstops/
---
## Paragraph::GetEffectiveTabStops method


Gibt ein Array aller Tabstopps zurück, die auf diesen Absatz angewendet wurden, einschließlich solcher, die indirekt über Stile oder Listen angewendet wurden.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::TabStop>> Aspose::Words::Paragraph::GetEffectiveTabStops()
```


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

* Class [TabStop](../../tabstop/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
