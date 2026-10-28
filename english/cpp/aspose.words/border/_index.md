---
title: Aspose::Words::Border class
linktitle: Border
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Border class. Represents a border of an object. To learn more, visit the Programming with Documents documentation article in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words/border/
---
## Border class


Represents a border of an object. 
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) documentation article.

```cpp
class Border : public InternableComplexAttr,
               public IComplexAttr
```

## Methods

| Method | Description |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Resets border properties to default values. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Determines whether the specified object is equal in value to the current object. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Border\> \&) | Determines whether the specified border is equal in value to the current border. |
| [GetHashCode](./gethashcode/)() const override | Serves as a hash function for this type. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| static [Type](./type/)() |  |
| [get_Color](./get_color/)() | Gets or sets the border color. |
| [get_DistanceFromText](./get_distancefromtext/)() | Gets or sets distance of the border from text or from the page edge in points. |
| [get_IsVisible](./get_isvisible/)() | Returns **true** if the [LineStyle](./get_linestyle/) is not [None](../linestyle/). |
| [get_LineStyle](./get_linestyle/)() | Gets or sets the border style. |
| [get_LineWidth](./get_linewidth/)() | Gets or sets the border width in points. |
| [get_Shadow](./get_shadow/)() | Gets or sets a value indicating whether the border has a shadow. |
| [get_ThemeColor](./get_themecolor/)() | Gets or sets the theme color in the applied color scheme that is associated with this Border object. |
| [get_TintAndShade](./get_tintandshade/)() | Gets or sets a double value that lightens or darkens a color. |
| [set_Color](./set_color/)(System::Drawing::Color) | Sets the border color. |
| [set_DistanceFromText](./set_distancefromtext/)(double) | Sets distance of the border from text or from the page edge in points. |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::LineStyle) | Sets the border style. |
| [set_LineWidth](./set_linewidth/)(double) | Sets the border width in points. |
| [set_Shadow](./set_shadow/)(bool) | Sets a value indicating whether the border has a shadow. |
| [set_ThemeColor](./set_themecolor/)(Aspose::Words::Themes::ThemeColor) | Sets the theme color in the applied color scheme that is associated with this Border object. |
| [set_TintAndShade](./set_tintandshade/)(double) | Sets a double value that lightens or darkens a color. |
| [GetType](../internablecomplexattr/gettype/)() const override |  |
| [Is](../internablecomplexattr/is/)(const System::TypeInfo \&) const override |  |
| static [Type](../internablecomplexattr/type/)() |  |
## Remarks


Borders can be applied to various document elements including paragraph, run of text inside a paragraph or a table cell.
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

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
