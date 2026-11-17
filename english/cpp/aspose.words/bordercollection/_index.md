---
title: Aspose::Words::BorderCollection class
linktitle: BorderCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BorderCollection class. A collection of Border objects. To learn more, visit the Programming with Documents documentation article in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words/bordercollection/
---
## BorderCollection class


A collection of [Border](../border/) objects. 
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) documentation article.

```cpp
class BorderCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Border>>
```

## Methods

| Method | Description |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Removes all borders of an object. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::BorderCollection\> \&) | Compares collections of borders. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object that can be used to iterate over all borders in the collection. |
| [get_Bottom](./get_bottom/)() | Gets the bottom border. |
| [get_Color](./get_color/)() | Gets or sets the border color. |
| [get_Count](./get_count/)() | Gets the number of borders in the collection. |
| [get_DistanceFromText](./get_distancefromtext/)() | Gets or sets distance of the border from text in points. |
| [get_Horizontal](./get_horizontal/)() | Gets the horizontal border that is used between cells or conforming paragraphs. |
| [get_Left](./get_left/)() | Gets the left border. |
| [get_LineStyle](./get_linestyle/)() | Gets or sets the border style. |
| [get_LineWidth](./get_linewidth/)() | Gets or sets the border width in points. |
| [get_Right](./get_right/)() | Gets the right border. |
| [get_Shadow](./get_shadow/)() | Gets or sets a value indicating whether the border has a shadow. |
| [get_Top](./get_top/)() | Gets the top border. |
| [get_Vertical](./get_vertical/)() | Gets the vertical border that is used between cells. |
| [idx_get](./idx_get/)(Aspose::Words::BorderType) | Retrieves a [Border](../border/) object by border type. |
| [idx_get](./idx_get/)(int32_t) | Retrieves a [Border](../border/) object by index. |
| [set_Color](./set_color/)(System::Drawing::Color) | Sets the border color. |
| [set_DistanceFromText](./set_distancefromtext/)(double) | Sets distance of the border from text in points. |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::LineStyle) | Sets the border style. |
| [set_LineWidth](./set_linewidth/)(double) | Sets the border width in points. |
| [set_Shadow](./set_shadow/)(bool) | Sets a value indicating whether the border has a shadow. |
## Remarks

 Different document elements have different borders. For example, [ParagraphFormat](../paragraphformat/) has [Bottom](./get_bottom/), [Left](./get_left/), [Right](./get_right/) and [Top](./get_top/) borders. You can specify different formatting for each border independently or enumerate through all borders and apply same formatting. 
## Examples


Shows how to insert a paragraph with a top border.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(LineStyle::DashSmallGap);
// Set ThemeColor only when LineWidth or LineStyle setted.
topBorder->set_ThemeColor(ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```
## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
