---
title: get_Underline
second_title: Aspose.Words for C++ API Reference
description: Gets/sets underline type for the current font.
type: docs
weight: 313
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->set_Underline(Underline::Dash);
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Size(32);

// The builder applies formatting to its current paragraph and any new text added by it afterward.
builder->Writeln(u"Large, blue, and underlined text.");

doc->Save(ArtifactsDir + u"DocumentBuilder.InsertUnderline.docx");
```

## See Also

* Enum [Underline](../../underline/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
