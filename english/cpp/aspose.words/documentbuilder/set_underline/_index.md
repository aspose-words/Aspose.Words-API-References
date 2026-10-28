---
title: Aspose::Words::DocumentBuilder::set_Underline method
linktitle: set_Underline
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::set_Underline method. Gets/sets underline type for the current font in C++.'
type: docs
weight: 95000
url: /cpp/aspose.words/documentbuilder/set_underline/
---
## DocumentBuilder::set_Underline method


Gets/sets underline type for the current font.

```cpp
void Aspose::Words::DocumentBuilder::set_Underline(Aspose::Words::Underline value)
```

## Examples


Shows how to format text inserted by a document builder.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->set_Underline(Underline::Dash);
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Size(32);

// The builder applies formatting to its current paragraph and any new text added by it afterward.
builder->Writeln(u"Large, blue, and underlined text.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertUnderline.docx");
```
## See Also

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
