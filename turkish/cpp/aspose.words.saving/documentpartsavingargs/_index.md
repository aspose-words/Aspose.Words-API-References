---
title: "Aspose::Words::Saving::DocumentPartSavingArgs sınıfı"
linktitle: "DocumentPartSavingArgs"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::DocumentPartSavingArgs sınıfı. DocumentPartSaving() geri araması için veri sağlar. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.saving/documentpartsavingargs/
---
## DocumentPartSavingArgs class


[DocumentPartSaving()](../idocumentpartsavingcallback/documentpartsaving/) geri araması için veri sağlar. Daha fazla bilgi edinmek için [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/) dokümantasyon makalesini ziyaret edin.

```cpp
class DocumentPartSavingArgs : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Document](./get_document/)() const | Kaydedilen belge nesnesini alır. |
| [get_DocumentPartFileName](./get_documentpartfilename/)() const | Belge parçasının kaydedileceği dosya adını (yol olmadan) alır veya ayarlar. |
| [get_DocumentPartStream](./get_documentpartstream/)() const | Belge parçasının kaydedileceği akışı belirtmeye izin verir. |
| [get_KeepDocumentPartStreamOpen](./get_keepdocumentpartstreamopen/)() const | Aspose.Words'ün belge parçasını kaydettikten sonra akışı açık tutup tutmayacağını belirtir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DocumentPartFileName](./set_documentpartfilename/)(const System::String\&) | [Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName](./get_documentpartfilename/) için ayarlayıcı. |
| [set_DocumentPartStream](./set_documentpartstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | [Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream](./get_documentpartstream/) için ayarlayıcı. |
| [set_DocumentPartStream](./set_documentpartstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_KeepDocumentPartStreamOpen](./set_keepdocumentpartstreamopen/)(bool) | [Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen](./get_keepdocumentpartstreamopen/) için ayarlayıcı. |
| static [Type](./type/)() |  |
## Açıklamalar


Aspose.Words bir belgeyi HTML veya ilgili formatlara kaydettiğinde ve [DocumentSplitCriteria](../htmlsaveoptions/get_documentsplitcriteria/) belirtilmişse, belge parçalara bölünür ve varsayılan olarak her belge parçası ayrı bir dosyaya kaydedilir.

[DocumentPartSavingArgs](./) sınıfı, her belge parçasının nasıl kaydedileceğini kontrol etmenizi sağlar. Dosya adlarının nasıl oluşturulacağını yeniden tanımlamanıza veya kendi akış nesnelerinizi sağlayarak belge parçalarının dosyalara kaydedilmesini tamamen önlemenize olanak tanır.

Belge parçalarını dosyalar yerine akışlara kaydetmek için, [DocumentPartStream](./get_documentpartstream/) özelliğini kullanın.
## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
