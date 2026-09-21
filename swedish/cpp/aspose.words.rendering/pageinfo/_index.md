---
title: "Aspose::Words::Rendering::PageInfo klass"
linktitle: "PageInfo"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Rendering::PageInfo klass. Representerar information om en specifik dokumentsida. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.rendering/pageinfo/
---
## PageInfo class


Representerar information om en specifik dokumentsida. För att lära dig mer, besök dokumentationsartikeln [Rendering](https://docs.aspose.com/words/cpp/rendering/).

```cpp
class PageInfo : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Colored](./get_colored/)() | Returnerar **true** om sidan innehåller färgat innehåll. |
| [get_HeightInPoints](./get_heightinpoints/)() | Hämtar sidans höjd i punkter. |
| [get_Landscape](./get_landscape/)() const | Returnerar **true** om sidans orientering som specificerats i dokumentet för denna sida är liggande. |
| [get_PaperSize](./get_papersize/)() | Hämtar papperstorleken som en uppräkning. |
| [get_PaperTray](./get_papertray/)() const | Hämtar pappersfacket (behållaren) för den här sidan enligt vad som anges i dokumentet. Värdet är specifikt för implementationen (skrivaren). |
| [get_SizeInPoints](./get_sizeinpoints/)() const | Hämtar sidstorleken i punkter. |
| [get_WidthInPoints](./get_widthinpoints/)() | Hämtar sidens bredd i punkter. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float) | Beräknar sidstorleken i pixlar för en angiven zoomfaktor och upplösning. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float, float) | Beräknar sidstorleken i pixlar för en angiven zoomfaktor och upplösning. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Anmärkningar


Sidans bredd och höjd som returneras av detta objekt representerar den "slutgiltiga" storleken på sidan, t.ex. de är redan roterade till rätt orientering.

## Se även

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
