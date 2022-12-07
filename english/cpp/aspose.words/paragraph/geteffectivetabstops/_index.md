---
title: GetEffectiveTabStops
second_title: Aspose.Words for C++ API Reference
description: Returns array of all tab stops applied to this paragraph, including applied indirectly by styles or lists.
type: docs
weight: 326
url: /cpp/aspose.words/paragraph/geteffectivetabstops/
---
## Paragraph::GetEffectiveTabStops method


Returns array of all tab stops applied to this paragraph, including applied indirectly by styles or lists.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::TabStop>> Aspose::Words::Paragraph::GetEffectiveTabStops()
```


## Examples



Shows how to set custom tab stops for a paragraph. 
```cpp
auto doc = MakeObject<Document>();
SharedPtr<Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// If we are in a paragraph with no tab stops in this collection,
// the cursor will jump 36 points each time we press the Tab key in Microsoft Word.
ASSERT_EQ(0, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetEffectiveTabStops()->get_Length());

// We can add custom tab stops in Microsoft Word if we enable the ruler via the "View" tab.
// Each unit on this ruler is two default tab stops, which is 72 points.
// We can add custom tab stops programmatically like this.
SharedPtr<TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_TabStops();
tabStops->Add(72, TabAlignment::Left, TabLeader::Dots);
tabStops->Add(216, TabAlignment::Center, TabLeader::Dashes);
tabStops->Add(360, TabAlignment::Right, TabLeader::Line);

// We can see these tab stops in Microsoft Word by enabling the ruler via "View" -> "Show" -> "Ruler".
ASSERT_EQ(3, para->GetEffectiveTabStops()->get_Length());

// Any tab characters we add will make use of the tab stops on the ruler and may,
// depending on the tab leader's value, leave a line between the tab departure and arrival destinations.
para->AppendChild(MakeObject<Run>(doc, u"\tTab 1\tTab 2\tTab 3"));

doc->Save(ArtifactsDir + u"Paragraph.TabStops.docx");
```

## See Also

* Class [TabStop](../../tabstop/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
