---
title: "Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName metodu"
linktitle: "get_ExportGeneratorName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName metodu. True olduğunda, Aspose.Words'in adını ve sürümünü oluşturulan dosyalara gömerir. Varsayılan değer C++'ta true'dur."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.saving/saveoptions/get_exportgeneratorname/
---
## SaveOptions::get_ExportGeneratorName method


**true** olduğunda, Aspose.Words'un adının ve sürümünün oluşturulan dosyalara gömülmesini sağlar. Varsayılan değer **true**'dur.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName() const
```


## Örnekler



Aspose.Words'in adını ve sürümünün oluşturulan dosyalara eklenmesini nasıl devre dışı bırakacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Sonucu nasıl kontrol edeceğinizi öğrenmek için https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/ adresini kullanın.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_ExportGeneratorName(false);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
```

## Ayrıca Bakınız

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
