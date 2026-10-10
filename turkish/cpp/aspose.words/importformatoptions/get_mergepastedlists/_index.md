---
title: "Aspose::Words::ImportFormatOptions::get_MergePastedLists yöntemi"
linktitle: "get_MergePastedLists"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ImportFormatOptions::get_MergePastedLists yöntemi. Yapıştırılan listelerin çevredeki listelerle birleştirilip birleştirilmeyeceğini belirten bir boolean değer alır veya ayarlar. Varsayılan değer C++'ta false'tur."
type: docs
weight: 8000
url: /tr/cpp/aspose.words/importformatoptions/get_mergepastedlists/
---
## ImportFormatOptions::get_MergePastedLists method


Yapıştırılan listelerin çevredeki listelerle birleştirileceğini belirten bir boolean değer alır veya ayarlar. Varsayılan değer **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_MergePastedLists() const
```


## Örnekler



Bir belgeden listelerin nasıl birleştirileceğini gösterir.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List destination.docx");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_MergePastedLists(true);

// "MergePastedLists" özelliğini "true" olarak ayarlayın, yapıştırılan listeler çevredeki listelerle birleştirilecektir.
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, options);

dstDoc->Save(get_ArtifactsDir() + u"Document.MergePastedLists.docx");
```

## Ayrıca Bakınız

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
