---
title: "Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream yöntemi"
linktitle: "get_DocumentPartStream"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream yöntemi. C++'ta belge parçasının kaydedileceği akışı belirtmeye olanak tanır."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.saving/documentpartsavingargs/get_documentpartstream/
---
## DocumentPartSavingArgs::get_DocumentPartStream method


Belge parçasının kaydedileceği akışı belirtmeye izin verir.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream() const
```

## Açıklamalar


Bu özellik, HTML dışa aktarımı sırasında belge parçalarını dosyalar yerine akışlara kaydetmenizi sağlar.

Varsayılan değer **null**'dır. Bu özellik **null** olduğunda, belge parçası [DocumentPartFileName](../get_documentpartfilename/) özelliğinde belirtilen bir dosyaya kaydedilir.

HTML formatında bir akışa kaydetme, [Save()](../) veya [Save()](../) tarafından istendiğinde ve ilk belge parçası kaydedilmek üzereyken, Aspose.Words burada çağıran tarafından ilk olarak verilen ana çıktı akışını önerir.

HTML tabanlı bir konteyner formatı olan EPUB formatına kaydedilirken, tüm yan parçalar tek bir çıktı paketine kapsülleninceği için [DocumentPartStream](./) belirtilemez.

## Ayrıca Bakınız

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
