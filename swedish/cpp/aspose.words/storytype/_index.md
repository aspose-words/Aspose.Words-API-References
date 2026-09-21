---
title: "Aspose::Words::StoryType enum"
linktitle: "StoryType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::StoryType enum. Texten i ett Word-dokument lagras i berättelser. StoryType identifierar en berättelse i C++."
type: docs
weight: 117000
url: /sv/cpp/aspose.words/storytype/
---
## StoryType enum


Texten i ett Word-dokument lagras i berättelser. [StoryType](./) identifierar en berättelse.

```cpp
enum class StoryType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | 0 | Standardvärde. Det finns ingen sådan berättelse i dokumentet. |
| MainText | 1 | Innehåller dokumentets huvudtext, representerad av [Body](../body/). |
| Footnotes | 2 | Innehåller fotnotstext, representerad av [Footnote](../../aspose.words.notes/footnote/). |
| Endnotes | 3 | Innehåller slutnotstext, representerad av [Footnote](../../aspose.words.notes/footnote/). |
| Comments | 4 | Innehåller dokumentkommentarer (anteckningar), representerade av [Comment](../comment/). |
| Textbox | 5 | Innehåller form- eller textrutetext, representerad av [Shape](../../aspose.words.drawing/shape/). |
| EvenPagesHeader | 6 | Innehåller texten för jämna sidors sidhuvud, representerad av [HeaderFooter](../headerfooter/). |
| PrimaryHeader | 7 | Innehåller texten för det primära sidhuvudet. När sidhuvudet är olika för udda och jämna sidor, innehåller det texten för udda sidors sidhuvud. Representerad av [HeaderFooter](../headerfooter/). |
| EvenPagesFooter | 8 | Innehåller texten för jämna sidors sidfot, representerad av [HeaderFooter](../headerfooter/). |
| PrimaryFooter | 9 | Innehåller texten för det primära sidfoten. När sidfoten är olika för udda och jämna sidor, innehåller den texten för udda sidors sidfot. Representerad av [HeaderFooter](../headerfooter/). |
| FirstPageHeader | 10 | Innehåller texten för första sidans sidhuvud, representerad av [HeaderFooter](../headerfooter/). |
| FirstPageFooter | 11 | Innehåller texten i den första sidans sidfot, representerad av [HeaderFooter](../headerfooter/). |
| FootnoteSeparator | 12 | Innehåller texten för fotnotsavgränsaren. |
| FootnoteContinuationSeparator | 13 | Innehåller texten för fotnotens fortsättningsavgränsare. |
| FootnoteContinuationNotice | 14 | Innehåller texten för fotnotens fortsättningsmeddelandeavgränsare. |
| EndnoteSeparator | 15 | Innehåller texten för slutnotavgränsaren. |
| EndnoteContinuationSeparator | 16 | Innehåller texten för slutnotens fortsättningsavgränsare. |
| EndnoteContinuationNotice | 17 | Innehåller texten för slutnotens fortsättningsmeddelandeavgränsare. |


## Exempel



Visar hur man tar bort alla former från en nod.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Använd en DocumentBuilder för att infoga en form. Detta är en inline-form,
// som har ett föräldra-Paragraph, som är ett barnnod till den första sektionens Body.
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// Vi kan ta bort alla former från de underordnade styckena i detta Body.
ASSERT_EQ(Aspose::Words::StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
