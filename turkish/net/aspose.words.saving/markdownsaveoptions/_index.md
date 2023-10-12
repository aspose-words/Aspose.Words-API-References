---
title: Class MarkdownSaveOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.MarkdownSaveOptions sınıf. Bir belgeyi kaydederken ek seçenekleri belirtmek için sınıfMarkdown format.
type: docs
weight: 5280
url: /tr/net/aspose.words.saving/markdownsaveoptions/
---
## MarkdownSaveOptions class

Bir belgeyi kaydederken ek seçenekleri belirtmek için sınıfMarkdown format.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Kaydetme Seçeneklerini Belirtin](https://docs.aspose.com/words/net/specify-save-options/) dokümantasyon makalesi.

```csharp
public class MarkdownSaveOptions : TxtSaveOptionsBase
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [MarkdownSaveOptions](markdownsaveoptions/)() | Bu sınıfın, bir document dosyasını kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Markdown format. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Kaydedildikten sonra TrueType yazı tiplerini bir belgeye gömerken PostScript ana hatlarıyla yazı tiplerinin gömülmesine izin verilip verilmeyeceğini belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`YANLIŞ` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Varsayılan şablonun yolunu alır veya ayarlar (dosya adı dahil). Bu özellik için varsayılan değer: **boş dize** (Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | 3B efektlerin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | DrawingML efektlerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | DrawingML şekillerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [Encoding](../../aspose.words.saving/txtsaveoptionsbase/encoding/) { get; set; } | Metin formatlarında dışa aktarırken kullanılacak kodlamayı belirtir. Varsayılan değer: **Kodlama.UTF8** . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Ne zaman`doğru` , Aspose.Words'ün adının ve sürümünün üretilen dosyalara yerleştirilmesine neden olur. Varsayılan değer:`doğru` . |
| [ExportHeadersFootersMode](../../aspose.words.saving/txtsaveoptionsbase/exportheadersfootersmode/) { get; set; } | Üstbilgilerin ve altbilgilerin metin formatlarına aktarılma yöntemini belirtir. Varsayılan değer:PrimaryOnly . |
| [ExportImagesAsBase64](../../aspose.words.saving/markdownsaveoptions/exportimagesasbase64/) { get; set; } | Görüntülerin çıktı dosyasına Base64 formatında kaydedilip kaydedilmeyeceğini belirtir. Varsayılan değer:`YANLIŞ` . |
| [ForcePageBreaks](../../aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/) { get; set; } | Dışa aktarma sırasında sayfa sonlarının korunup korunmayacağını belirtmenize olanak tanır. |
| [ImageSavingCallback](../../aspose.words.saving/markdownsaveoptions/imagesavingcallback/) { get; set; } | Bir belge 'ye kaydedildiğinde görüntülerin nasıl kaydedileceğini kontrol etmenize izin verirMarkdown format. |
| [ImagesFolder](../../aspose.words.saving/markdownsaveoptions/imagesfolder/) { get; set; } | Bir belgeyi 'ye aktarırken görüntülerin kaydedildiği fiziksel klasörü belirtir.Markdown biçim. Varsayılan boş bir dizedir. |
| [ImagesFolderAlias](../../aspose.words.saving/markdownsaveoptions/imagesfolderalias/) { get; set; } | Bir belgeye yazılan görüntü URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan, boş bir dizedir. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Mürekkep (InkML) nesnelerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [ListExportMode](../../aspose.words.saving/markdownsaveoptions/listexportmode/) { get; set; } | Liste öğelerinin çıktı dosyasına nasıl yazılacağını belirtir. Varsayılan değer:MarkdownSyntax . |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Belgeyi kaydetmeden önce bellek optimizasyonunun gerçekleştirilip gerçekleştirilmeyeceğini belirleyen değeri alır veya ayarlar. Bu özellik için varsayılan değer:`YANLIŞ` . |
| [ParagraphBreak](../../aspose.words.saving/txtsaveoptionsbase/paragraphbreak/) { get; set; } | Metin formatlarında dışa aktarırken paragraf sonu olarak kullanılacak dizeyi belirtir. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Ne zaman`doğru` uygulanabilir olduğu yerde güzel formatlarda çıktı. Varsayılan değer:`YANLIŞ` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Bir belge kaydedilirken çağrılır ve kaydetme işlemiyle ilgili verileri kabul eder. |
| override [SaveFormat](../../aspose.words.saving/markdownsaveoptions/saveformat/) { get; set; } | Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. YalnızcaMarkdown . |
| [TableContentAlignment](../../aspose.words.saving/markdownsaveoptions/tablecontentalignment/) { get; set; } | Tablolara dışa aktarılırken içeriklerin nasıl hizalanacağını belirten bir değer alır veya ayarlar.Markdown format. Varsayılan değer:Auto . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Bir DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik`hükümsüz` ve hiçbir geçici dosya kullanılmaz. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Bir değer alır veya ayarlar.[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) özellik kaydedilmeden önce güncellenir. Varsayılan değer:`YANLIŞ` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Belgeyi sabit bir sayfa formatında kaydetmeden önce belirli türlerdeki alanların güncellenmesi gerekip gerekmediğini belirleyen bir değer alır veya ayarlar. Bu özellik için varsayılan değer:`doğru` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Bir değer alır veya ayarlar.[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) özellik kaydedilmeden önce güncellenir. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Bir değer alır veya ayarlar.[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) özellik kaydedilmeden önce güncellenir. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Oluşturma için kenar yumuşatma kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Yüksek kaliteli (yani yavaş) oluşturma algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |

### Ayrıca bakınız

* class [TxtSaveOptionsBase](../txtsaveoptionsbase/)
* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


