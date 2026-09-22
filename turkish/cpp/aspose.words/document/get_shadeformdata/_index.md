---
title: "Aspose::Words::Document::get_ShadeFormData metodu"
linktitle: "get_ShadeFormData"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_ShadeFormData metodu. C++'ta form alanlarında gri gölgelendirmeyi açıp açmayacağını belirtir."
type: docs
weight: 49000
url: /tr/cpp/aspose.words/document/get_shadeformdata/
---
## Document::get_ShadeFormData method


Form alanlarında gri gölgelendirmeyi açıp açmayacağını belirtir.

```cpp
bool Aspose::Words::Document::get_ShadeFormData()
```


## Örnekler



Form alanlarına gri gölgelendirme nasıl uygulanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world! ");
builder->InsertTextInput(u"My form field", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Text contents of form field, which are shaded in grey by default.", 0);

// Gri gölgelendirmeyi kapatabiliriz, böylece yer işareti eklenmiş metin diğer metinle karışır.
doc->set_ShadeFormData(useGreyShading);
doc->Save(get_ArtifactsDir() + u"Document.ShadeFormData.docx");
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
