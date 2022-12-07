---
title: get_Borders
second_title: Aspose.Words for C++ API Reference
description: Gets collection of borders of the paragraph.
type: docs
weight: 79
url: /cpp/aspose.words/paragraphformat/get_borders/
---
## ParagraphFormat::get_Borders method


Gets collection of borders of the paragraph.

```cpp
System::SharedPtr<Aspose::Words::BorderCollection> Aspose::Words::ParagraphFormat::get_Borders()
```


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

* Class [BorderCollection](../../bordercollection/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
