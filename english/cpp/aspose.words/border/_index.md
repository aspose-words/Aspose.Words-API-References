---
title: Border
second_title: Aspose.Words for C++ API Reference
description: Represents a border of an object.
type: docs
weight: 79
url: /cpp/aspose.words/border/
---
## Border class


Represents a border of an object.

```cpp
class Border : public Aspose::Words::InternableComplexAttr, public Aspose::Words::IComplexAttr
```

## Methods

| Method | Description |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Resets border properties to default values. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Border\>\&) | Determines whether the specified border is equal in value to the current border. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Determines whether the specified object is equal in value to the current object. |
| [get_Color](./get_color/)() | Gets or sets the border color. |
| [get_DistanceFromText](./get_distancefromtext/)() | Gets or sets distance of the border from text or from the page edge in points. |
| [get_IsVisible](./get_isvisible/)() | Returns true if the LineStyle is not **LineStyle.None**. |
| [get_LineStyle](./get_linestyle/)() | Gets or sets the border style. |
| [get_LineWidth](./get_linewidth/)() | Gets or sets the border width in points. |
| [get_Shadow](./get_shadow/)() | Gets or sets a value indicating whether the border has a shadow. |
| [GetHashCode](./gethashcode/)() const override | Serves as a hash function for this type. |
| [set_Color](./set_color/)(System::Drawing::Color) | Setter for [Aspose::Words::Border::get_Color](./get_color/). |
| [set_DistanceFromText](./set_distancefromtext/)(double) | Setter for [Aspose::Words::Border::get_DistanceFromText](./get_distancefromtext/). |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::LineStyle) | Setter for [Aspose::Words::Border::get_LineStyle](./get_linestyle/). |
| [set_LineWidth](./set_linewidth/)(double) | Setter for [Aspose::Words::Border::get_LineWidth](./get_linewidth/). |
| [set_Shadow](./set_shadow/)(bool) | Setter for [Aspose::Words::Border::get_Shadow](./get_shadow/). |

Borders can be applied to various document elements including paragraph, run of text inside a paragraph or a table cell.

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

