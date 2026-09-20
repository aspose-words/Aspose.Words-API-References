---
title: "метод Aspose::Words::Saving::SaveOutputParameters::get_ContentType"
linktitle: "get_ContentType"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Saving::SaveOutputParameters::get_ContentType. Возвращает строку Content-Type (Internet Media Type), которая определяет тип сохранённого документа в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.saving/saveoutputparameters/get_contenttype/
---
## SaveOutputParameters::get_ContentType method


Возвращает строку Content-Type (Internet Media Type), определяющую тип сохранённого документа.

```cpp
System::String Aspose::Words::Saving::SaveOutputParameters::get_ContentType() const
```


## Примеры



Показывает, как получить доступ к параметрам вывода операции сохранения документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// После сохранения документа мы можем получить доступ к типу Интернет‑медиа (MIME‑type) вновь созданного выходного документа.
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.doc");

ASSERT_EQ(u"application/msword", parameters->get_ContentType());

// Это свойство меняется в зависимости от формата сохранения.
parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.pdf");

ASSERT_EQ(u"application/pdf", parameters->get_ContentType());
```

## См. также

* Class [SaveOutputParameters](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
