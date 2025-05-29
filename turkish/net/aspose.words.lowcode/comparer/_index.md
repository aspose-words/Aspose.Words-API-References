---
title: Comparer Class
linktitle: Comparer
articleTitle: Comparer
second_title: .NET için Aspose.Words
description: Aspose.Words LowCode Comparer sınıfıyla belgeleri zahmetsizce karşılaştırın. Sorunsuz belge analizi ve işbirliği için güçlü yöntemlerin kilidini açın.
type: docs
weight: 4210
url: /tr/net/aspose.words.lowcode/comparer/
---
## Comparer class

Belgeleri karşılaştırmayı amaçlayan yöntemler sağlar.

```csharp
public class Comparer : Processor
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| static [Create](../../aspose.words.lowcode/comparer/create/#create)() | Dönüştürücü işlemcinin yeni bir örneğini oluşturur. |
| static [Create](../../aspose.words.lowcode/comparer/create/#create_1)(*[ComparerContext](../comparercontext/)*) | Karşılaştırıcı işlemcinin yeni örneğini oluşturur. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | İşlemci eylemini yürüt. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | İşleme için giriş belgesini belirtir. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | İşleme için giriş belgesini belirtir. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Çıktı Belge akışları listesini belirtir. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Çıktı Belge akışları listesini belirtir. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | İşlemci için çıkış akışını belirtir. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | İşlemci için çıkış akışını belirtir. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | İşlemci için çıktı dosyasını belirtir. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | İşlemci için çıktı dosyasını belirtir. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare_4)(*string, string, string, string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | İki belgeyi ek seçeneklerle karşılaştırır ve farklılıkları belirtilen çıktı dosyasına kaydeder, değişiklikleri bir dizi düzenleme ve biçim revizyonu olarak üretir. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare)(*Stream, Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Akışlardan yüklenen iki belgeyi ek seçeneklerle karşılaştırır ve farklılıkları belirtilen kaydetme biçiminde sağlanan çıktı akışına kaydeder, değişiklikleri bir dizi düzenleme ve biçim revizyonu olarak üretir. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare_1)(*Stream, Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Akışlardan yüklenen iki belgeyi ek seçeneklerle karşılaştırır ve farklılıkları belirtilen kaydetme biçiminde sağlanan çıktı akışına kaydeder, değişiklikleri bir dizi düzenleme ve biçim revizyonu olarak üretir. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare_2)(*string, string, string, [SaveFormat](../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | İki belgeyi ek seçeneklerle karşılaştırır ve farklılıkları belirtilen çıktı dosyasına sağlanan kaydetme biçiminde kaydeder, değişiklikleri bir dizi düzenleme ve biçim revizyonu olarak üretir. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare_3)(*string, string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | İki belgeyi ek seçeneklerle karşılaştırır ve farklılıkları belirtilen çıktı dosyasına sağlanan kaydetme biçiminde kaydeder, değişiklikleri bir dizi düzenleme ve biçim revizyonu olarak üretir. |
| static [CompareToImages](../../aspose.words.lowcode/comparer/comparetoimages/#comparetoimages)(*Stream, Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | İki belgeyi karşılaştırır ve farkları resim olarak kaydeder. Döndürülen dizideki her öğe, çıktının resim olarak işlenen tek bir sayfasını temsil eder. |
| static [CompareToImages](../../aspose.words.lowcode/comparer/comparetoimages/#comparetoimages_1)(*string, string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | İki belgeyi karşılaştırır ve farkları resim olarak kaydeder. Döndürülen dizideki her öğe, çıktının resim olarak işlenen tek bir sayfasını temsil eder. |

### Ayrıca bakınız

* class [Processor](../processor/)
* ad alanı [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../)
