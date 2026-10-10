---
title: "Aspose::Words::Saving::ResourceSavingArgs class"
linktitle: "ResourceSavingArgs"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::ResourceSavingArgs sınıfı. ResourceSaving() olayı için veri sağlar. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 27000
url: /tr/cpp/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class


Veri sağlar [ResourceSaving()](../iresourcesavingcallback/resourcesaving/) olayı için. Daha fazla bilgi edinmek için [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/) belge makalesini ziyaret edin.

```cpp
class ResourceSavingArgs : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Document](./get_document/)() const | Şu anda kaydedilen belge nesnesini alır. |
| [get_KeepResourceStreamOpen](./get_keepresourcestreamopen/)() const | Aspose.Words'ün akışı açık tutup tutmayacağını veya bir kaynak kaydedildikten sonra kapatıp kapatmayacağını belirtir. |
| [get_ResourceFileName](./get_resourcefilename/)() const | Kaynağın kaydedileceği dosya adını (yol olmadan) alır veya ayarlar. |
| [get_ResourceFileUri](./get_resourcefileuri/)() const | Belgeden kaynak dosyasına referans vermek için kullanılan birleşik kaynak tanımlayıcısını (URI) alır veya ayarlar. |
| [get_ResourceStream](./get_resourcestream/)() const | Kaynağın kaydedileceği akışı belirtmeye izin verir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_KeepResourceStreamOpen](./set_keepresourcestreamopen/)(bool) | Ayarlayıcı: [Aspose::Words::Saving::ResourceSavingArgs::get_KeepResourceStreamOpen](./get_keepresourcestreamopen/). |
| [set_ResourceFileName](./set_resourcefilename/)(const System::String\&) | Ayarlayıcı: [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName](./get_resourcefilename/). |
| [set_ResourceFileUri](./set_resourcefileuri/)(const System::String\&) | Ayarlayıcı: [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri](./get_resourcefileuri/). |
| [set_ResourceStream](./set_resourcestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Ayarlayıcı: [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream](./get_resourcestream/). |
| [set_ResourceStream](./set_resourcestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |
## Açıklamalar


Varsayılan olarak, Aspose.Words bir belgeyi sabit sayfa HTML, SVG veya Markdown olarak kaydettiğinde, her kaynağı ayrı bir dosyaya kaydeder. Aspose.Words, belge dosya adını ve benzersiz bir numarayı kullanarak belgede bulunan her kaynak için benzersiz dosya adı oluşturur.

[ResourceSavingArgs](./) allows to redefine how resource file names are generated or to completely circumvent saving of resources into files by providing your own stream objects.

Kendi mantığınızı kaynak dosya adları oluşturmak için uygulamak üzere [ResourceFileName](./get_resourcefilename/) özelliğini kullanın.

Dosyalar yerine akışlara kaynakları kaydetmek için [ResourceStream](./get_resourcestream/) özelliğini kullanın.
## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
