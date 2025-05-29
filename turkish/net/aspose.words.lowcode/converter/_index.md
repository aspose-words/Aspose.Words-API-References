---
title: Converter Class
linktitle: Converter
articleTitle: Converter
second_title: .NET için Aspose.Words
description: Aspose.Words.LowCode.Converter ile çeşitli belge türlerini zahmetsizce dönüştürün. Sorunsuz entegrasyon için yalnızca bir satır kod kullanarak iş akışınızı basitleştirin.
type: docs
weight: 4230
url: /tr/net/aspose.words.lowcode/converter/
---
## Converter class

Tek bir kod satırı kullanarak çeşitli farklı türdeki belgeleri dönüştürmeyi amaçlayan bir yöntem grubunu temsil eder.

```csharp
public class Converter : Processor
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| static [Create](../../aspose.words.lowcode/converter/create/#create)() | Dönüştürücü işlemcinin yeni bir örneğini oluşturur. |
| static [Create](../../aspose.words.lowcode/converter/create/#create_1)(*[ConverterContext](../convertercontext/)*) | Dönüştürücü işlemcinin yeni bir örneğini oluşturur. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | İşlemci eylemini yürüt. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | İşleme için giriş belgesini belirtir. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | İşleme için giriş belgesini belirtir. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Çıktı Belge akışları listesini belirtir. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Çıktı Belge akışları listesini belirtir. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | İşlemci için çıkış akışını belirtir. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | İşlemci için çıkış akışını belirtir. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | İşlemci için çıktı dosyasını belirtir. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | İşlemci için çıktı dosyasını belirtir. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_4)(*string, string*) | Belirtilen giriş-çıkış dosya adlarını ve uzantılarını kullanarak verilen giriş belgesini çıkış belgesine dönüştürür. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Belirtilen giriş ve çıkış akışlarını kullanarak verilen giriş belgesini tek bir çıkış belgesine dönüştürür. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_2)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen giriş ve çıkış akışlarını kullanarak verilen giriş belgesini tek bir çıkış belgesine dönüştürür. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_5)(*string, string, [SaveFormat](../../aspose.words/saveformat/)*) | Belirtilen giriş-çıkış dosya adlarını ve son belge biçimini kullanarak verilen giriş belgesini çıkış belgesine dönüştürür. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_6)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen giriş-çıkış dosya adlarını ve kaydetme seçeneklerini kullanarak belirtilen giriş belgesini çıkış belgesine dönüştürür. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/), Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen giriş ve çıkış akışlarını kullanarak verilen giriş belgesini tek bir çıkış belgesine dönüştürür. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_3)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/), string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen giriş çıktı dosya adlarını ve yükleme/kaydetme seçeneklerini kullanarak belirtilen giriş belgesini çıkış belgesine dönüştürür. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_1)(*[Document](../../aspose.words/document/), [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Belirtilen belgenin sayfalarını belirtilen kaydetme seçeneklerini kullanarak görüntülere dönüştürür ve görüntüleri içeren bir akış dizisi döndürür. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages)(*[Document](../../aspose.words/document/), [SaveFormat](../../aspose.words/saveformat/)*) | Belirtilen belgenin sayfalarını belirtilen formattaki görüntülere dönüştürür ve görüntüleri içeren bir akış dizisi döndürür. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_4)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Belirtilen giriş akışının sayfalarını belirtilen kaydetme seçeneklerini kullanarak görüntülere dönüştürür ve görüntüleri içeren bir akış dizisi döndürür. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_3)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Belirtilen giriş akışının sayfalarını belirtilen biçimdeki görüntülere dönüştürür ve görüntüleri içeren bir akış dizisi döndürür. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_6)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Belirtilen giriş dosyasının sayfalarını belirtilen kaydetme seçeneklerini kullanarak görüntülere dönüştürür ve görüntüleri içeren bir akış dizisi döndürür. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_5)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Belirtilen giriş dosyasının sayfalarını belirtilen formattaki görüntülere dönüştürür ve görüntüleri içeren bir akış dizisi döndürür. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_2)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/), [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Belirtilen giriş akışının sayfalarını, sağlanan yükleme ve kaydetme seçeneklerini kullanarak görüntülere dönüştürür ve görüntüleri içeren bir akış dizisi döndürür. |

## Notlar

Belirtilen giriş ve çıkış dosyaları veya akışları, istenen kaydetme biçimiyle birlikte, , bir biçimdeki verilen giriş belgesini, belirtilen diğer biçimdeki çıkış belgesine dönüştürmek için kullanılır.

Dönüştürme işlevi 35'ten fazla farklı dosya biçimini destekler.

The[`ConvertToImages`](./converttoimages/)yöntem grubu, her sayfanın ayrı bir görüntü dosyasına dönüştürülmesiyle belgeleri görüntülere dönüştürmek için tasarlanmıştır. Bu yöntemler ayrıca PDF belgelerini belge modeline yüklemeden doğrudan sabit sayfa biçimlerine dönüştürür. Bu da hem performansı hem de doğruluğu artırır.

İle[`PageSet`](../../aspose.words.saving/imagesaveoptions/pageset/), resimlere dönüştürülecek belirli bir sayfa kümesini belirtebilirsiniz.

### Ayrıca bakınız

* class [Processor](../processor/)
* ad alanı [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../)
