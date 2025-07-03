---
title: Aspose::Words::DocumentBuilder::get_Underline method
linktitle: get_Underline
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::get_Underline method. Gets/sets underline type for the current font in C++.'
type: docs
weight: 26000
url: /cpp/aspose.words/documentbuilder/get_underline/
---
## DocumentBuilder::get_Underline method


Gets/sets underline type for the current font.

```cpp
Aspose::Words::Underline Aspose::Words::DocumentBuilder::get_Underline()
```


## Examples



Shows how to format text inserted by a document builder. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->set_Underline(Aspose::Words::Underline::Dash);
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Size(32);

// The builder applies formatting to its current paragraph and any new text added by it afterward.
builder->Writeln(u"Large, blue, and underlined text.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertUnderline.docx");
```

## See Also

* Enum [Underline](../../underline/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
