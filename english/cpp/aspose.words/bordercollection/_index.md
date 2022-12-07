---
title: BorderCollection
second_title: Aspose.Words for C++ API Reference
description: A collection of Border objects. To learn more, visit the  documentation article.
type: docs
weight: 92
url: /cpp/aspose.words/bordercollection/
---
## BorderCollection class


A collection of [Border](../border/) objects. To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) documentation article.

```cpp
class BorderCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Border>>
```

## Methods

| Method | Description |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Removes all borders of an object. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::BorderCollection\>\&) | Compares collections of borders. |
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
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object that can be used to iterate over all borders in the collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::BorderType) | Retrieves a [Border](../border/) object by border type. |
| [idx_get](./idx_get/)(int32_t) | Retrieves a [Border](../border/) object by index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Setter for [Aspose::Words::BorderCollection::get_Color](./get_color/). |
| [set_DistanceFromText](./set_distancefromtext/)(double) | Setter for [Aspose::Words::BorderCollection::get_DistanceFromText](./get_distancefromtext/). |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::LineStyle) | Setter for [Aspose::Words::BorderCollection::get_LineStyle](./get_linestyle/). |
| [set_LineWidth](./set_linewidth/)(double) | Setter for [Aspose::Words::BorderCollection::get_LineWidth](./get_linewidth/). |
| [set_Shadow](./set_shadow/)(bool) | Setter for [Aspose::Words::BorderCollection::get_Shadow](./get_shadow/). |
| static [Type](./type/)() |  |

## Examples



Shows how to insert a paragraph with a top border. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->idx_get(BorderType::Top);
topBorder->set_Color(System::Drawing::Color::get_Red());
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(LineStyle::DashSmallGap);

builder->Writeln(u"Text with a red top border.");

doc->Save(ArtifactsDir + u"Border.ParagraphTopBorder.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words](../../)
