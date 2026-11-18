---
title: Aspose::Words::LineStyle enum
linktitle: LineStyle
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LineStyle enum. Specifies line style of a Border in C++.'
type: docs
weight: 96000
url: /cpp/aspose.words/linestyle/
---
## LineStyle enum


Specifies line style of a [Border](../border/).

```cpp
enum class LineStyle : int
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| DashDotStroker | 23 |  |
| DashLargeGap | 7 |  |
| DashSmallGap | 22 |  |
| Dot | 6 |  |
| DotDash | 8 |  |
| DotDotDash | 9 |  |
| Double | 3 |  |
| DoubleWave | 21 |  |
| Emboss3D | 24 |  |
| Engrave3D | 25 |  |
| Hairline | 5 |  |
| Inset | 27 |  |
| None | 0 |  |
| Outset | 26 |  |
| Single | 1 |  |
| Thick | 2 |  |
| ThickThinLargeGap | 18 |  |
| ThickThinMediumGap | 15 |  |
| ThickThinSmallGap | 12 |  |
| ThinThickLargeGap | 17 |  |
| ThinThickMediumGap | 14 |  |
| ThinThickSmallGap | 11 |  |
| ThinThickThinLargeGap | 19 |  |
| ThinThickThinMediumGap | 16 |  |
| ThinThickThinSmallGap | 13 |  |
| Triple | 10 |  |
| Wave | 20 |  |

## Examples


Shows how to insert a string surrounded by a border into a document.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```
## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
