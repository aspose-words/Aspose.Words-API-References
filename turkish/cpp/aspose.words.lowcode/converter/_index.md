---
title: "Aspose::Words::LowCode::Converter sınıfı"
linktitle: "Converter"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::LowCode::Converter sınıfı. C++'ta tek bir kod satırıyla çeşitli belge türlerini dönüştürmek için tasarlanmış bir yöntem grubunu temsil eder."
type: docs
weight: 600
url: /tr/cpp/aspose.words.lowcode/converter/
---
## Converter class


Tek bir kod satırı kullanarak çeşitli farklı belge türlerini dönüştürmek için tasarlanmış bir yöntem grubunu temsil eder.

```cpp
class Converter : public Aspose::Words::LowCode::Processor
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| static [Convert](./convert/)(const System::String\&, const System::String\&) | Belirtilen giriş ve çıkış dosya adlarını ve uzantılarını kullanarak verilen giriş belgesini çıkış belgesine dönüştürür. |
| static [Convert](./convert/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | Belirtilen giriş ve çıkış dosya adlarını ve son belge formatını kullanarak verilen giriş belgesini çıktı belgesine dönüştürür. |
| static [Convert](./convert/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Belirtilen giriş ve çıkış dosya adlarını ve kaydetme seçeneklerini kullanarak verilen giriş belgesini çıktı belgesine dönüştürür. |
| static [Convert](./convert/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Belirtilen giriş ve çıkış dosya adlarını ve yükleme/kaydetme seçeneklerini kullanarak verilen giriş belgesini çıktı belgesine dönüştürür. |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Belirtilen giriş ve çıkış akışlarını kullanarak verilen giriş belgesini tek bir çıktı belgesine dönüştürür. |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Belirtilen giriş ve çıkış akışlarını kullanarak verilen giriş belgesini tek bir çıktı belgesine dönüştürür. |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Belirtilen giriş ve çıkış akışlarını kullanarak verilen giriş belgesini tek bir çıktı belgesine dönüştürür. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&) | Belirtilen giriş dosyasının sayfalarını görüntü dosyalarına dönüştürür. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | Belirtilen giriş dosyasının sayfalarını belirtilen formatta görüntü dosyalarına dönüştürür. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Belirtilen giriş dosyasının sayfalarını belirtilen kaydetme seçeneklerini kullanarak görüntü dosyalarına dönüştürür. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Belirtilen giriş dosyasının sayfalarını sağlanan yükleme ve kaydetme seçeneklerini kullanarak görüntü dosyalarına dönüştürür. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, Aspose::Words::SaveFormat) | Belirtilen giriş dosyasının sayfalarını belirtilen formatta görüntülere dönüştürür ve görüntüleri içeren akışların bir dizisini döndürür. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Belirtilen giriş dosyasının sayfalarını belirtilen kaydetme seçeneklerini kullanarak görüntülere dönüştürür ve görüntüleri içeren akışların bir dizisini döndürür. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Belirtilen giriş akışının sayfalarını belirtilen formatta görüntülere dönüştürür ve görüntüleri içeren akışların bir dizisini döndürür. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Belirtilen giriş akışının sayfalarını belirtilen kaydetme seçeneklerini kullanarak görüntülere dönüştürür ve görüntüleri içeren akışların bir dizisini döndürür. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Belirtilen giriş akışının sayfalarını sağlanan yükleme ve kaydetme seçeneklerini kullanarak görüntülere dönüştürür ve görüntüleri içeren akışların bir dizisini döndürür. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::SaveFormat) | Belirtilen belgenin sayfalarını belirtilen formatta görüntülere dönüştürür ve görüntüleri içeren akışların bir dizisini döndürür. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Belirtilen belgenin sayfalarını belirtilen kaydetme seçeneklerini kullanarak görüntülere dönüştürür ve görüntüleri içeren akışların bir dizisini döndürür. |
| static [Create](./create/)() | Dönüştürücü işlemcinin yeni bir örneğini oluşturur. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ConverterContext\>\&) | Dönüştürücü işlemcinin yeni bir örneğini oluşturur. |
| [Execute](../processor/execute/)() | İşlemci eylemini yürütün. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Belirtilen iptal belirteci kullanılarak belge işleme görevini iptal etmeye izin veren işlemci eylemini yürütün. |
| [From](../processor/from/)(const System::String\&) | İşleme için giriş belgesini belirtir. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | İşleme için giriş belgesini belirtir. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | İşleme için giriş belgesini belirtir. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | İşleme için giriş belgesini belirtir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [To](../processor/to/)(const System::String\&) | İşlemci için çıkış dosyasını belirtir. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | İşlemci için çıkış dosyasını belirtir. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | İşlemci için çıkış dosyasını belirtir. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | İşlemci için çıkış akışını belirtir. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | İşlemci için çıkış akışını belirtir. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Açıklamalar


Belirtilen giriş ve çıkış dosyaları veya akışları, istenen kaydetme formatı ile birlikte, verilen giriş belgesini bir formattan diğer belirtilen formata dönüştürmek için kullanılır.

Dönüştürme işlevi 35+ farklı dosya formatını destekler.

Bu [ConvertToImages()](../) yöntem grubu, belgeleri görüntülere dönüştürmek için tasarlanmıştır; her sayfa ayrı bir görüntü dosyasına dönüştürülür. Bu yöntemler ayrıca PDF belgelerini belge modeline yüklemeden doğrudan sabit sayfa formatlarına dönüştürür, bu da performans ve doğruluğu artırır.

İle [PageSet](../../aspose.words.saving/imagesaveoptions/get_pageset/), görüntülere dönüştürmek için belirli bir sayfa kümesi belirtebilirsiniz.
## Ayrıca Bakınız

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
