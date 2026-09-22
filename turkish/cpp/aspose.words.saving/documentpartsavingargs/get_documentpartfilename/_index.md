---
title: "Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName metodu"
linktitle: "get_DocumentPartFileName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName metodu. C++'da belge parçasının kaydedileceği dosya adını (yol olmadan) alır veya ayarlar."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.saving/documentpartsavingargs/get_documentpartfilename/
---
## DocumentPartSavingArgs::get_DocumentPartFileName method


Belge parçasının kaydedileceği dosya adını (yol olmadan) alır veya ayarlar.

```cpp
System::String Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName() const
```

## Açıklamalar


Bu özellik, belge parçası dosya adlarının HTML veya EPUB dışa aktarma sırasında nasıl oluşturulduğunu yeniden tanımlamanıza olanak tanır.

Geri arama tetiklendiğinde, bu özellik Aspose.Words tarafından oluşturulan dosya adını içerir. Bu özelliğin değerini değiştirerek belge parçasını farklı bir dosyaya kaydedebilirsiniz. Her parça için dosya adının benzersiz olması gerektiğini unutmayın.

[DocumentPartFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name. If output document file name was not specified, for instance when saving to a stream, this file name is used only for referencing document parts. The same is true when saving to EPUB format.

## Ayrıca Bakınız

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
