---
title: Aspose::Words::Document::get_ShadeFormData method
linktitle: get_ShadeFormData
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::get_ShadeFormData method. Specifies whether to turn on the gray shading on form fields in C++.'
type: docs
weight: 49000
url: /cpp/aspose.words/document/get_shadeformdata/
---
## Document::get_ShadeFormData method


Specifies whether to turn on the gray shading on form fields.

```cpp
bool Aspose::Words::Document::get_ShadeFormData()
```


## Examples



Shows how to apply gray shading to form fields. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world! ");
builder->InsertTextInput(u"My form field", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Text contents of form field, which are shaded in grey by default.", 0);

// We can turn the grey shading off, so the bookmarked text will blend in with the other text.
doc->set_ShadeFormData(useGreyShading);
doc->Save(get_ArtifactsDir() + u"Document.ShadeFormData.docx");
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
