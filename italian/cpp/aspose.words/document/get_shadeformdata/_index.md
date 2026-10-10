---
title: "Aspose::Words::Document::get_ShadeFormData method"
linktitle: "get_ShadeFormData"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::get_ShadeFormData method. Specifica se attivare l'ombreggiatura grigia sui campi modulo in C++."
type: docs
weight: 49000
url: /it/cpp/aspose.words/document/get_shadeformdata/
---
## Document::get_ShadeFormData method


Specifica se attivare l'ombreggiatura grigia sui campi modulo.

```cpp
bool Aspose::Words::Document::get_ShadeFormData()
```


## Esempi



Mostra come applicare l'ombreggiatura grigia ai campi modulo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world! ");
builder->InsertTextInput(u"My form field", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Text contents of form field, which are shaded in grey by default.", 0);

// Possiamo disattivare l'ombreggiatura grigia, così il testo contrassegnato si fonderà con il resto del testo.
doc->set_ShadeFormData(useGreyShading);
doc->Save(get_ArtifactsDir() + u"Document.ShadeFormData.docx");
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
