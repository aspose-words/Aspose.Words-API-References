---
title: get_ShadeFormData
second_title: Aspose.Words for C++ API Reference
description: Specifies whether to turn on the gray shading on form fields.
type: docs
weight: 586
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Write(u"Hello world! ");
builder->InsertTextInput(u"My form field", TextFormFieldType::Regular, u"", u"Text contents of form field, which are shaded in grey by default.", 0);

// We can turn the grey shading off, so the bookmarked text will blend in with the other text.
doc->set_ShadeFormData(useGreyShading);
doc->Save(ArtifactsDir + u"Document.ShadeFormData.docx");
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
