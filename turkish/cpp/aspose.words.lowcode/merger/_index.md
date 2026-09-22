---
title: "Aspose::Words::LowCode::Merger sınıfı"
linktitle: "Merger"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::LowCode::Merger sınıfı. C++'da çeşitli farklı belge türlerini tek bir çıktı belgesine birleştirmeyi amaçlayan bir dizi yöntemi temsil eder."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.lowcode/merger/
---
## Merger class


Çeşitli farklı belge türlerini tek bir çıktı belgesine birleştirmek için tasarlanmış bir yöntem grubunu temsil eder.

```cpp
class Merger : public Aspose::Words::LowCode::Processor
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| static [Create](./create/)() | Posta birleştirici işlemcisinin yeni bir örneğini oluşturur. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::MergerContext\>\&) | Posta birleştirici işlemcisinin yeni bir örneğini oluşturur. |
| [Execute](../processor/execute/)() | İşlemci eylemini yürütün. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Belirtilen iptal belirteci kullanılarak belge işleme görevini iptal etmeye izin veren işlemci eylemini yürütün. |
| [From](../processor/from/)(const System::String\&) | İşleme için giriş belgesini belirtir. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | İşleme için giriş belgesini belirtir. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | İşleme için giriş belgesini belirtir. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | İşleme için giriş belgesini belirtir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | Belirtilen giriş ve çıkış dosya adlarını kullanarak verilen giriş belgelerini tek bir çıkış belgesinde birleştirir, [KeepSourceFormatting](../mergeformatmode/) kullanarak. |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, Aspose::Words::SaveFormat, Aspose::Words::LowCode::MergeFormatMode) | Belirtilen giriş ve çıkış dosya adları ile son belge formatını kullanarak verilen giriş belgelerini tek bir çıkış belgesinde birleştirir. |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Belirtilen giriş ve çıkış dosya adları ve kaydetme seçeneklerini kullanarak verilen giriş belgelerini tek bir çıkış belgesinde birleştirir. |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Belirtilen giriş ve çıkış dosya adları ve kaydetme seçeneklerini kullanarak verilen giriş belgelerini tek bir çıkış belgesinde birleştirir. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::String\>\&, Aspose::Words::LowCode::MergeFormatMode) | Verilen giriş belgelerini tek bir belgede birleştirir ve son belgenin [Document](../../aspose.words/document/) örneğini döndürür. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Verilen giriş belgelerini tek bir belgede birleştirir ve son belgenin [Document](../../aspose.words/document/) örneğini döndürür. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Verilen giriş belgelerini tek bir belgede birleştirir ve son belgenin [Document](../../aspose.words/document/) örneğini döndürür. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, Aspose::Words::SaveFormat) | Belirtilen giriş ve çıkış akışlarını ve son belge formatını kullanarak verilen giriş belgelerini tek bir çıkış belgesinde birleştirir. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Belirtilen giriş ve çıkış akışlarını ve kaydetme seçeneklerini kullanarak verilen giriş belgelerini tek bir çıkış belgesinde birleştirir. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Belirtilen giriş ve çıkış akışlarını ve kaydetme seçeneklerini kullanarak verilen giriş belgelerini tek bir çıkış belgesinde birleştirir. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Verilen giriş belgelerini tek bir belgede birleştirir ve son belgenin [Document](../../aspose.words/document/) örneğini döndürür. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Verilen giriş belgelerini tek bir belgede birleştirir ve son belgenin [Document](../../aspose.words/document/) örneğini döndürür. |
| static [MergeToImages](./mergetoimages/)(const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Belirtilen giriş ve çıkış dosya adları ve kaydetme seçeneklerini kullanarak verilen giriş belgelerini tek bir çıkış belgesinde birleştirir. Çıktıyı görüntülere render eder. |
| static [MergeToImages](./mergetoimages/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Belirtilen görüntü kaydetme seçeneklerini kullanarak verilen giriş belge akışlarını tek bir çıkış belgesinde birleştirir. Çıktıyı görüntülere render eder. |
| [To](../processor/to/)(const System::String\&) | İşlemci için çıkış dosyasını belirtir. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | İşlemci için çıkış dosyasını belirtir. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | İşlemci için çıkış dosyasını belirtir. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | İşlemci için çıkış akışını belirtir. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | İşlemci için çıkış akışını belirtir. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Açıklamalar


Belirtilen giriş ve çıkış dosyaları veya akışları, istenen birleştirme ve kaydetme seçenekleriyle birlikte, verilen giriş belgelerini tek bir çıkış belgesinde birleştirmek için kullanılır.

Birleştirme işlevi 35'ten fazla farklı dosya formatını destekler.
## Ayrıca Bakınız

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
