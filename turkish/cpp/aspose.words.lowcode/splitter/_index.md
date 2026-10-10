---
title: "Aspose::Words::LowCode::Splitter sınıfı"
linktitle: "Splitter"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::LowCode::Splitter sınıfı. C++'ta farklı kriterlere göre belgeleri parçalara bölmek için yöntemler sağlar."
type: docs
weight: 1500
url: /tr/cpp/aspose.words.lowcode/splitter/
---
## Splitter class


Belgeleri farklı kriterlere göre parçalara bölmek için tasarlanmış yöntemler sağlar.

```cpp
class Splitter : public Aspose::Words::LowCode::Processor
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::SplitterContext\>\&) | Bölücü işlemcinin yeni bir örneğini oluşturur. |
| [Execute](../processor/execute/)() | İşlemci eylemini yürütün. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Belirtilen iptal belirteci kullanılarak belge işleme görevini iptal etmeye izin veren işlemci eylemini yürütün. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, int32_t, int32_t) | Belge dosyasından belirtilen bir sayfa aralığını çıkarır ve çıkarılan sayfaları yeni bir dosyaya kaydeder. Çıktı dosya formatı, çıktı dosya adının uzantısına göre belirlenir. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, int32_t, int32_t) | Belge dosyasından belirtilen bir sayfa aralığını çıkarır ve çıkarılan sayfaları belirtilen kaydetme formatını kullanarak yeni bir dosyaya kaydeder. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) | Belge dosyasından belirtilen bir sayfa aralığını çıkarır ve çıkarılan sayfaları belirtilen kaydetme formatını kullanarak yeni bir dosyaya kaydeder. |
| static [ExtractPages](./extractpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, int32_t, int32_t) | Belge akışından belirtilen bir sayfa aralığını çıkarır ve çıkarılan sayfaları belirtilen kaydetme formatını kullanarak bir çıktı akışına kaydeder. |
| static [ExtractPages](./extractpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) | Belge akışından belirtilen bir sayfa aralığını çıkarır ve çıkarılan sayfaları belirtilen kaydetme formatını kullanarak bir çıktı akışına kaydeder. |
| [From](../processor/from/)(const System::String\&) | İşleme için giriş belgesini belirtir. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | İşleme için giriş belgesini belirtir. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | İşleme için giriş belgesini belirtir. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | İşleme için giriş belgesini belirtir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&) | Belgedeki boş sayfaları kaldırır ve çıktıyı kaydeder. Kaldırılan sayfa numaralarının bir listesini döndürür. |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | Belgedeki boş sayfaları kaldırır ve çıktıyı belirtilen formatta kaydeder. Kaldırılan sayfa numaralarının bir listesini döndürür. |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Belgedeki boş sayfaları kaldırır ve çıktıyı belirtilen formatta kaydeder. Kaldırılan sayfa numaralarının bir listesini döndürür. |
| static [RemoveBlankPages](./removeblankpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Giriş akışında sağlanan bir belgedeki boş sayfaları kaldırır ve güncellenen belgeyi belirtilen kaydetme formatında bir çıktı akışına kaydeder. Kaldırılan sayfa numaralarının bir listesini döndürür. |
| static [RemoveBlankPages](./removeblankpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Giriş akışında sağlanan bir belgedeki boş sayfaları kaldırır ve güncellenen belgeyi belirtilen kaydetme formatında bir çıktı akışına kaydeder. Kaldırılan sayfa numaralarının bir listesini döndürür. |
| static [Split](./split/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Belgeyi belirtilen bölme seçeneklerine göre birden çok parçaya ayırır ve ortaya çıkan parçaları dosyalara kaydeder. Çıktı dosya formatı, çıktı dosya adının uzantısına göre belirlenir. |
| static [Split](./split/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Belgeyi belirtilen bölme seçeneklerine göre birden çok parçaya ayırır ve ortaya çıkan parçaları belirtilen kaydetme formatında dosyalara kaydeder. |
| static [Split](./split/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Belgeyi belirtilen bölme seçeneklerine göre birden çok parçaya ayırır ve ortaya çıkan parçaları belirtilen kaydetme formatında dosyalara kaydeder. |
| static [Split](./split/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Bir giriş akışındaki belgeyi belirtilen bölme seçeneklerine göre birden çok parçaya ayırır ve ortaya çıkan parçaları belirtilen kaydetme formatında akış dizisi olarak döndürür. |
| static [Split](./split/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Bir giriş akışındaki belgeyi belirtilen bölme seçeneklerine göre birden çok parçaya ayırır ve ortaya çıkan parçaları belirtilen kaydetme formatında akış dizisi olarak döndürür. |
| [To](../processor/to/)(const System::String\&) | İşlemci için çıkış dosyasını belirtir. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | İşlemci için çıkış dosyasını belirtir. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | İşlemci için çıkış dosyasını belirtir. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | İşlemci için çıkış akışını belirtir. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | İşlemci için çıkış akışını belirtir. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
