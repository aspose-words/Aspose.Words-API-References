---
title: "Aspose::Words::Document::get_ShadeFormData метод"
linktitle: "get_ShadeFormData"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::get_ShadeFormData метод. Указывает, включать ли серую заливку в полях формы в C++."
type: docs
weight: 49000
url: /ru/cpp/aspose.words/document/get_shadeformdata/
---
## Document::get_ShadeFormData method


Указывает, включать ли серую заливку в полях формы.

```cpp
bool Aspose::Words::Document::get_ShadeFormData()
```


## Примеры



Показывает, как применить серую заливку к полям формы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world! ");
builder->InsertTextInput(u"My form field", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Text contents of form field, which are shaded in grey by default.", 0);

// Мы можем отключить серую заливку, чтобы закладка текста слилась с остальным текстом.
doc->set_ShadeFormData(useGreyShading);
doc->Save(get_ArtifactsDir() + u"Document.ShadeFormData.docx");
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
