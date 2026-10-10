---
title: "Aspose::Words::IDocumentReaderPlugin::Read metodu"
linktitle: "Oku"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::IDocumentReaderPlugin::Read metodu. Belirtilen akıştan verileri C++'da Document örneğine okur."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/idocumentreaderplugin/read/
---
## IDocumentReaderPlugin::Read method


Belirtilen akıştan verileri [Document](../../document/) örneğine okur.

```cpp
virtual void Aspose::Words::IDocumentReaderPlugin::Read(System::SharedPtr<System::IO::Stream> src, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<Aspose::Words::Document> document)=0
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| src | System::SharedPtr\<System::IO::Stream\> | Belgeyi okumak için kaynak akış. |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | Belgeyi yüklemek için ek yükleme seçenekleri. |
| document | System::SharedPtr\<Aspose::Words::Document\> | Verilerin okunacağı [Document](../../document/) sınıfının örneği. Eğer örnek bazı içeriklere sahipse, kaynak akıştan gelen verilerle üzerine yazılacaktır. |

## Ayrıca Bakınız

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../../document/)
* Interface [IDocumentReaderPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
