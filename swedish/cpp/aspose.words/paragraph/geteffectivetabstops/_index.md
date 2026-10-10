---
title: "Aspose::Words::Paragraph::GetEffectiveTabStops metod"
linktitle: "GetEffectiveTabStops"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Paragraph::GetEffectiveTabStops metod. Returnerar en array med alla tabbstopp som tillämpas på detta stycke, inklusive de som tillämpas indirekt via stilar eller listor i C++."
type: docs
weight: 26000
url: /sv/cpp/aspose.words/paragraph/geteffectivetabstops/
---
## Paragraph::GetEffectiveTabStops method


Returnerar en array med alla tabbstopp som tillämpats på detta stycke, inklusive de som tillämpats indirekt via stilar eller listor.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::TabStop>> Aspose::Words::Paragraph::GetEffectiveTabStops()
```


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

* Class [TabStop](../../tabstop/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
