---
title: "Aspose::Words::TabLeader enum"
linktitle: "TabLeader"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::TabLeader enum. Anger typen av ledarlinje som visas under tabulatortecknet i C++."
type: docs
weight: 121000
url: /sv/cpp/aspose.words/tableader/
---
## TabLeader enum


Anger typen av ledarlinje som visas under tabulatortecknet.

```cpp
enum class TabLeader
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | 0 | Ingen ledarlinje visas. |
| Punkter | 1 | Ledarlinjen består av punkter. |
| Streck | 2 | Ledarlinjen består av streck. |
| Linje | 3 | Ledarlinjen är en enkel linje. |
| Heavy | 4 | Ledarlinjen är en enkel tjock linje. |
| MiddleDot | 5 | Ledarlinjen består av mittenpunkter. |


## Exempel



Visar hur man ställer in anpassade tabbstopp för ett stycke.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Om vi är i ett stycke utan tabbstopp i denna samling,
// kommer markören att hoppa 36 punkter varje gång vi trycker på Tab-tangenten i Microsoft Word.
ASSERT_EQ(0, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetEffectiveTabStops()->get_Length());

// Vi kan lägga till anpassade tabbstopp i Microsoft Word om vi aktiverar linjalen via \"View\"-fliken.
// Varje enhet på denna linjal motsvarar två standardtabbstopp, vilket är 72 punkter.
// Vi kan lägga till anpassade tabbstopp programatiskt på detta sätt.
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_TabStops();
tabStops->Add(72, Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dots);
tabStops->Add(216, Aspose::Words::TabAlignment::Center, Aspose::Words::TabLeader::Dashes);
tabStops->Add(360, Aspose::Words::TabAlignment::Right, Aspose::Words::TabLeader::Line);

// Vi kan se dessa tabbstopp i Microsoft Word genom att aktivera linjalen via \"View\" -> \"Show\" -> \"Ruler\".
ASSERT_EQ(3, para->GetEffectiveTabStops()->get_Length());

// Alla tab-tecken vi lägger till kommer att använda tabbstoppen på linjalen och kan,
// beroende på tabbledarens värde, lämna en rad mellan tabbavfärd och ankomstdestinationer.
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"\tTab 1\tTab 2\tTab 3"));

doc->Save(get_ArtifactsDir() + u"Paragraph.TabStops.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
