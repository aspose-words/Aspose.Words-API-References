---
title: LineStyle
second_title: Aspose.Words for C++ API Reference
description: Specifies line style of a Border.
type: docs
weight: 1249
url: /cpp/aspose.words/linestyle/
---
## LineStyle enum


Specifies line style of a [Border](../border/).

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 |  |
| Single | 1 |  |
| Thick | 2 |  |
| Double | 3 |  |
| Hairline | 5 |  |
| Dot | 6 |  |
| DashLargeGap | 7 |  |
| DotDash | 8 |  |
| DotDotDash | 9 |  |
| Triple | 10 |  |
| ThinThickSmallGap | 11 |  |
| ThickThinSmallGap | 12 |  |
| ThinThickThinSmallGap | 13 |  |
| ThinThickMediumGap | 14 |  |
| ThickThinMediumGap | 15 |  |
| ThinThickThinMediumGap | 16 |  |
| ThinThickLargeGap | 17 |  |
| ThickThinLargeGap | 18 |  |
| ThinThickThinLargeGap | 19 |  |
| Wave | 20 |  |
| DoubleWave | 21 |  |
| DashSmallGap | 22 |  |
| DashDotStroker | 23 |  |
| Emboss3D | 24 |  |
| Engrave3D | 25 |  |
| Outset | 26 |  |
| Inset | 27 |  |


## Examples




Shows how to insert a string surrounded by a border into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(ArtifactsDir + u"Border.FontBorder.docx");
```

