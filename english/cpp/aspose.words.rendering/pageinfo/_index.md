---
title: PageInfo
second_title: Aspose.Words for C++ API Reference
description: Represents information about a particular document page.
type: docs
weight: 27
url: /cpp/aspose.words.rendering/pageinfo/
---
## PageInfo class


Represents information about a particular document page.

```cpp
class PageInfo : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_HeightInPoints](./get_heightinpoints/)() | Gets the height of the page in points. |
| [get_Landscape](./get_landscape/)() const | Returns true if the page orientation specified in the document for this page is landscape. |
| [get_PaperSize](./get_papersize/)() | Gets the paper size as enumeration. |
| [get_PaperTray](./get_papertray/)() const | Gets the paper tray (bin) for this page as specified in the document. The value is implementation (printer) specific. |
| [get_SizeInPoints](./get_sizeinpoints/)() const | Gets the page size in points. |
| [get_WidthInPoints](./get_widthinpoints/)() | Gets the width of the page in points. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float) | Calculates the page size in pixels for a specified zoom factor and resolution. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float, float) | Calculates the page size in pixels for a specified zoom factor and resolution. |
## Remarks


The page width and height returned by this object represent the "final" size of the page e.g. they are already rotated to the correct orientation.

## See Also

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words](../../)
