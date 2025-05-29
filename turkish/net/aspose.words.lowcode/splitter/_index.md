---
title: Splitter Class
linktitle: Splitter
articleTitle: Splitter
second_title: .NET için Aspose.Words
description: Aspose.Words.LowCode.Splitter sınıfıyla belgeleri zahmetsizce bölün. Hassas belge yönetimi ve gelişmiş iş akışı verimliliği için çok yönlü yöntemlerden yararlanın.
type: docs
weight: 4420
url: /tr/net/aspose.words.lowcode/splitter/
---
## Splitter class

Belgeleri farklı ölçütler kullanarak parçalara ayırmayı amaçlayan yöntemler sağlar.

```csharp
public class Splitter : Processor
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| static [Create](../../aspose.words.lowcode/splitter/create/)(*[SplitterContext](../splittercontext/)*) | Ayırıcı işlemcinin yeni bir örneğini oluşturur. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | İşlemci eylemini yürüt. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | İşleme için giriş belgesini belirtir. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | İşleme için giriş belgesini belirtir. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Çıktı Belge akışları listesini belirtir. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Çıktı Belge akışları listesini belirtir. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | İşlemci için çıkış akışını belirtir. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | İşlemci için çıkış akışını belirtir. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | İşlemci için çıktı dosyasını belirtir. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | İşlemci için çıktı dosyasını belirtir. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_4)(*string, string, int, int*) | Bir belge dosyasından belirtilen bir sayfa aralığını ayıklar ve ayıklanan sayfaları yeni bir dosyaya kaydeder. Çıktı dosya biçimi, çıktı dosya adının uzantısı tarafından belirlenir. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), int, int*) | Bir belge akışından belirtilen sayfa aralığını ayıklar ve ayıklanan sayfaları belirtilen kaydetme biçimini kullanarak bir çıktı akışına kaydeder. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_1)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), int, int*) | Bir belge akışından belirtilen sayfa aralığını ayıklar ve ayıklanan sayfaları belirtilen kaydetme biçimini kullanarak bir çıktı akışına kaydeder. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_2)(*string, string, [SaveFormat](../../aspose.words/saveformat/), int, int*) | Bir belge dosyasından belirtilen sayfa aralığını ayıklar ve ayıklanan sayfaları belirtilen kaydetme biçimini kullanarak yeni bir dosyaya kaydeder. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_3)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), int, int*) | Bir belge dosyasından belirtilen sayfa aralığını ayıklar ve ayıklanan sayfaları belirtilen kaydetme biçimini kullanarak yeni bir dosyaya kaydeder. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_2)(*string, string*) | Belgeden boş sayfaları kaldırır ve çıktıyı kaydeder. Kaldırılan sayfa numaralarının bir listesini döndürür. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Giriş akışında sağlanan bir belgeden boş sayfaları kaldırır ve güncellenen belgeyi belirtilen kaydetme biçiminde bir çıktı akışına kaydeder. Kaldırılan sayfa numaralarının bir listesini döndürür. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_1)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Giriş akışında sağlanan bir belgeden boş sayfaları kaldırır ve güncellenen belgeyi belirtilen kaydetme biçiminde bir çıktı akışına kaydeder. Kaldırılan sayfa numaralarının bir listesini döndürür. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_3)(*string, string, [SaveFormat](../../aspose.words/saveformat/)*) | Belgeden boş sayfaları kaldırır ve çıktıyı belirtilen biçimde kaydeder. Kaldırılan sayfa numaralarının bir listesini döndürür. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_4)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belgeden boş sayfaları kaldırır ve çıktıyı belirtilen biçimde kaydeder. Kaldırılan sayfa numaralarının bir listesini döndürür. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split)(*Stream, [SaveFormat](../../aspose.words/saveformat/), [SplitOptions](../splitoptions/)*) | Belirtilen bölme seçeneklerine göre bir giriş akışından gelen belgeyi birden fazla parçaya böler ve ortaya çıkan parçaları belirtilen kaydetme biçiminde bir akış dizisi olarak döndürür. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_1)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), [SplitOptions](../splitoptions/)*) | Belirtilen bölme seçeneklerine göre bir giriş akışından gelen belgeyi birden fazla parçaya böler ve ortaya çıkan parçaları belirtilen kaydetme biçiminde bir akış dizisi olarak döndürür. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_2)(*string, string, [SplitOptions](../splitoptions/)*) | Belirtilen bölme seçeneklerine göre bir belgeyi birden fazla parçaya böler ve ortaya çıkan parçaları dosyalara kaydeder. Çıktı dosya biçimi, çıktı dosya adının uzantısı tarafından belirlenir. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_3)(*string, string, [SaveFormat](../../aspose.words/saveformat/), [SplitOptions](../splitoptions/)*) | Belirtilen bölme seçeneklerine göre bir belgeyi birden fazla parçaya böler ve ortaya çıkan parçaları belirtilen kaydetme biçimindeki dosyalara kaydeder. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_4)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), [SplitOptions](../splitoptions/)*) | Belirtilen bölme seçeneklerine göre bir belgeyi birden fazla parçaya böler ve ortaya çıkan parçaları belirtilen kaydetme biçimindeki dosyalara kaydeder. |

### Ayrıca bakınız

* class [Processor](../processor/)
* ad alanı [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../)
