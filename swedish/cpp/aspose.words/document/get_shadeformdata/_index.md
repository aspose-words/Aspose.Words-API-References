---
title: "Aspose::Words::Document::get_ShadeFormData metod"
linktitle: "get_ShadeFormData"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::get_ShadeFormData metod. Anger om grå skuggning på formulärfält ska slås på i C++."
type: docs
weight: 49000
url: /sv/cpp/aspose.words/document/get_shadeformdata/
---
## Document::get_ShadeFormData method


Anger om grå skuggning på formulärfält ska slås på.

```cpp
bool Aspose::Words::Document::get_ShadeFormData()
```


## Exempel



Visar hur man applicerar grå skuggning på formulärfält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world! ");
builder->InsertTextInput(u"My form field", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Text contents of form field, which are shaded in grey by default.", 0);

// Vi kan stänga av den grå skuggningen, så att den bokmärkta texten smälter in med den övriga texten.
doc->set_ShadeFormData(useGreyShading);
doc->Save(get_ArtifactsDir() + u"Document.ShadeFormData.docx");
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
