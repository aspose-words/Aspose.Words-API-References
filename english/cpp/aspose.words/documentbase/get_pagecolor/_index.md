---
title: get_PageColor
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the page color of the document. This property is a simpler version of BackgroundShape.
type: docs
weight: 79
url: /cpp/aspose.words/documentbase/get_pagecolor/
---
## DocumentBase::get_PageColor method


Gets or sets the page color of the document. This property is a simpler version of [BackgroundShape](../get_backgroundshape/).

```cpp
System::Drawing::Color Aspose::Words::DocumentBase::get_PageColor()
```

## Remarks


This property provides a simple way to specify a solid page color for the document. Setting this property creates and sets an appropriate [BackgroundShape](../get_backgroundshape/).

If the page color is not set (e.g. there is no background shape in the document) returns **Empty**.

## Examples



Shows how to set the background color for all pages of a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->set_PageColor(System::Drawing::Color::get_LightGray());

doc->Save(ArtifactsDir + u"DocumentBase.SetPageColor.docx");
```

## See Also

* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
