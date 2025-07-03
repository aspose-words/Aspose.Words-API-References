---
title: Aspose::Words::TabAlignment enum
linktitle: TabAlignment
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::TabAlignment enum. Specifies the alignment/type of a tab stop in C++.'
type: docs
weight: 120000
url: /cpp/aspose.words/tabalignment/
---
## TabAlignment enum


Specifies the alignment/type of a tab stop.

```cpp
enum class TabAlignment
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Left | 0 | Left-aligns the text after the tab stop. |
| Center | 1 | Centers the text around the tab stop. |
| Right | 2 | Right-aligns the text at the tab stop. |
| Decimal | 3 | Aligns the text at the decimal dot. |
| Bar | 4 | Draws a vertical bar at the tab stop position. |
| List | 6 | The tab is a delimiter between the number/bullet and text in a list item. |
| Clear | 7 | Clears any tab stop in this position. |


## Examples



Shows how to set custom tab stops for a paragraph. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// If we are in a paragraph with no tab stops in this collection,
// the cursor will jump 36 points each time we press the Tab key in Microsoft Word.
ASSERT_EQ(0, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetEffectiveTabStops()->get_Length());

// We can add custom tab stops in Microsoft Word if we enable the ruler via the "View" tab.
// Each unit on this ruler is two default tab stops, which is 72 points.
// We can add custom tab stops programmatically like this.
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_TabStops();
tabStops->Add(72, Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dots);
tabStops->Add(216, Aspose::Words::TabAlignment::Center, Aspose::Words::TabLeader::Dashes);
tabStops->Add(360, Aspose::Words::TabAlignment::Right, Aspose::Words::TabLeader::Line);

// We can see these tab stops in Microsoft Word by enabling the ruler via "View" -> "Show" -> "Ruler".
ASSERT_EQ(3, para->GetEffectiveTabStops()->get_Length());

// Any tab characters we add will make use of the tab stops on the ruler and may,
// depending on the tab leader's value, leave a line between the tab departure and arrival destinations.
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"\tTab 1\tTab 2\tTab 3"));

doc->Save(get_ArtifactsDir() + u"Paragraph.TabStops.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
