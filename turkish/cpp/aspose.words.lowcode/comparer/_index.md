---
title: "Aspose::Words::LowCode::Comparer class"
linktitle: "Comparer"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::LowCode::Comparer sınıfı. C++'ta belgeleri karşılaştırmak için tasarlanmış yöntemler sağlar."
type: docs
weight: 500
url: /tr/cpp/aspose.words.lowcode/comparer/
---
## Comparer class


Belgeleri karşılaştırmak için tasarlanmış yöntemler sağlar.

```cpp
class Comparer : public Aspose::Words::LowCode::Processor
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime) | İki belgeyi ek seçeneklerle karşılaştırır ve farkları belirtilen çıkış dosyasına kaydeder, değişiklikleri bir dizi düzenleme ve format revizyonu olarak üretir. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | İki belgeyi ek seçeneklerle karşılaştırır ve farkları belirtilen çıkış dosyasına kaydeder, değişiklikleri bir dizi düzenleme ve format revizyonu olarak üretir. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) | İki belgeyi ek seçeneklerle karşılaştırır ve farkları sağlanan kaydetme formatında belirtilen çıkış dosyasına kaydeder, değişiklikleri bir dizi düzenleme ve format revizyonu olarak üretir. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | İki belgeyi ek seçeneklerle karşılaştırır ve farkları sağlanan kaydetme formatında belirtilen çıkış dosyasına kaydeder, değişiklikleri bir dizi düzenleme ve format revizyonu olarak üretir. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) | İki belgeyi ek seçeneklerle karşılaştırır ve farkları sağlanan kaydetme formatında belirtilen çıkış dosyasına kaydeder, değişiklikleri bir dizi düzenleme ve format revizyonu olarak üretir. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | İki belgeyi ek seçeneklerle karşılaştırır ve farkları sağlanan kaydetme formatında belirtilen çıkış dosyasına kaydeder, değişiklikleri bir dizi düzenleme ve format revizyonu olarak üretir. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) | Akışlardan yüklenen iki belgeyi ek seçeneklerle karşılaştırır ve farkları belirtilen kaydetme formatında sağlanan çıkış akışına kaydeder, değişiklikleri bir dizi düzenleme ve format revizyonu olarak üretir. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Akışlardan yüklenen iki belgeyi ek seçeneklerle karşılaştırır ve farkları belirtilen kaydetme formatında sağlanan çıkış akışına kaydeder, değişiklikleri bir dizi düzenleme ve format revizyonu olarak üretir. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) | Akışlardan yüklenen iki belgeyi ek seçeneklerle karşılaştırır ve farkları belirtilen kaydetme formatında sağlanan çıkış akışına kaydeder, değişiklikleri bir dizi düzenleme ve format revizyonu olarak üretir. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Akışlardan yüklenen iki belgeyi ek seçeneklerle karşılaştırır ve farkları belirtilen kaydetme formatında sağlanan çıkış akışına kaydeder, değişiklikleri bir dizi düzenleme ve format revizyonu olarak üretir. |
| static [CompareToImages](./comparetoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) | İki belgeyi karşılaştırır ve farkları görüntüler olarak kaydeder. Döndürülen dizideki her öğe, çıktının bir sayfasının görüntü olarak render edilmesini temsil eder. |
| static [CompareToImages](./comparetoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | İki belgeyi karşılaştırır ve farkları görüntüler olarak kaydeder. Döndürülen dizideki her öğe, çıktının bir sayfasının görüntü olarak render edilmesini temsil eder. |
| static [CompareToImages](./comparetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) | İki belgeyi karşılaştırır ve farkları görüntüler olarak kaydeder. Döndürülen dizideki her öğe, çıktının bir sayfasının görüntü olarak render edilmesini temsil eder. |
| static [CompareToImages](./comparetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | İki belgeyi karşılaştırır ve farkları görüntüler olarak kaydeder. Döndürülen dizideki her öğe, çıktının bir sayfasının görüntü olarak render edilmesini temsil eder. |
| static [Create](./create/)() | Dönüştürücü işlemcinin yeni bir örneğini oluşturur. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ComparerContext\>\&) | Karşılaştırıcı işlemcinin yeni bir örneğini oluşturur. |
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
## Ayrıca Bakınız

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
