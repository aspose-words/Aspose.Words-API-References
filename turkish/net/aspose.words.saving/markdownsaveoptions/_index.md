---
title: Class MarkdownSaveOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.MarkdownSaveOptions sınıf. Bir belgeyi dosyaya kaydederken ek seçenekleri belirtmek için SınıfMarkdown biçim.
type: docs
weight: 5000
url: /tr/net/aspose.words.saving/markdownsaveoptions/
---
## MarkdownSaveOptions class

Bir belgeyi dosyaya kaydederken ek seçenekleri belirtmek için SınıfMarkdown biçim.

```csharp
public class MarkdownSaveOptions : TxtSaveOptionsBase
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [MarkdownSaveOptions](markdownsaveoptions/)() | Bu sınıfın, bir document dosyasını şuraya kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Markdown biçim. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | TrueType yazı tiplerini bir belgeye gömerken PostScript anahatlarıyla yazı tiplerinin gömülmesine izin verilip verilmeyeceğini belirten bir boole değeri alır veya ayarlar. Varsayılan değer şudur: **yanlış** . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Varsayılan şablonun yolunu alır veya ayarlar (dosya adı dahil). Bu özellik için varsayılan değer **boş dize** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | 3B efektlerin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | DrawingML efektlerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | DrawingML şekillerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [Encoding](../../aspose.words.saving/txtsaveoptionsbase/encoding/) { get; set; } | Metin biçimlerinde dışa aktarırken kullanılacak kodlamayı belirtir. Varsayılan değer **Kodlama.UTF8** . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Doğru olduğunda, Aspose.Words'ün adının ve sürümünün üretilen dosyalara gömülmesine neden olur. Varsayılan değerdir **doğru** . |
| [ExportHeadersFootersMode](../../aspose.words.saving/txtsaveoptionsbase/exportheadersfootersmode/) { get; set; } | Üstbilgilerin ve altbilgilerin metin biçimlerine dışa aktarılma şeklini belirtir. Varsayılan değerPrimaryOnly . |
| [ExportImagesAsBase64](../../aspose.words.saving/markdownsaveoptions/exportimagesasbase64/) { get; set; } | Görüntülerin çıktı dosyasına Base64 biçiminde kaydedilip kaydedilmeyeceğini belirtir. Varsayılan`yanlış` . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Hangi belge biçimlerinin eşlenmesine izin verildiğini belirleyen değeri alır veya ayarlar.[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Yalnızca varsayılan olarakFlatOpc belge biçiminin eşlenmesine izin verilir. |
| [ForcePageBreaks](../../aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/) { get; set; } | Dışa aktarma sırasında sayfa sonlarının korunup korunmayacağını belirtmeye izin verir. |
| [ImageSavingCallback](../../aspose.words.saving/markdownsaveoptions/imagesavingcallback/) { get; set; } | Bir belge konumuna kaydedildiğinde resimlerin nasıl kaydedileceğini kontrol etmenizi sağlarMarkdown biçim. |
| [ImagesFolder](../../aspose.words.saving/markdownsaveoptions/imagesfolder/) { get; set; } | Bir belgeyi öğesine dışa aktarırken görüntülerin kaydedildiği fiziksel klasörü belirtir.Markdown biçim. Varsayılan boş bir dizedir. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Mürekkep (InkML) nesnelerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Belgeyi kaydetmeden önce bellek optimizasyonunun yapılıp yapılmayacağını belirleyen değeri alır veya ayarlar. Bu özellik için varsayılan değer **yanlış** . |
| [ParagraphBreak](../../aspose.words.saving/txtsaveoptionsbase/paragraphbreak/) { get; set; } | Metin biçimlerinde dışa aktarırken paragraf sonu olarak kullanılacak dizeyi belirtir. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Ne zaman`doğru` , uygun olduğunda güzel biçimler çıktısı. Varsayılan değer **yanlış** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Bir belge kaydedilirken çağrılır ve ilerleme kaydetmeyle ilgili verileri kabul eder. |
| override [SaveFormat](../../aspose.words.saving/markdownsaveoptions/saveformat/) { get; set; } | Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. YalnızcaMarkdown . |
| [TableContentAlignment](../../aspose.words.saving/markdownsaveoptions/tablecontentalignment/) { get; set; } | Tablolara dışa aktarırken tabloların içindeki içeriğin nasıl hizalanacağını belirten bir değer alır veya ayarlar.Markdown format. Varsayılan değerAuto . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Bir DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik`hükümsüz` ve hiçbir geçici dosya kullanılmaz. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | olup olmadığını belirleyen bir değer alır veya ayarlar.[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) özellik kaydedilmeden önce güncellenir. Varsayılan değer false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Belgeyi sabit bir sayfa biçimine kaydetmeden önce belirli türlerdeki alanların güncellenmesi gerekip gerekmediğini belirleyen bir değer alır veya ayarlar. Bu özellik için varsayılan değer **doğru** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | olup olmadığını belirleyen bir değer alır veya ayarlar.[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) özellik kaydedilmeden önce güncellenir. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | olup olmadığını belirleyen bir değer alır veya ayarlar.[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) özellik kaydedilmeden önce güncellenir. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | İçeriğin olup olmadığını belirleyen değeri alır veya ayarlar.[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) kaydetmeden önce güncellenir. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | İşleme için kenar yumuşatma kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Yüksek kaliteli (yani yavaş) işleme algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |

### Ayrıca bakınız

* class [TxtSaveOptionsBase](../txtsaveoptionsbase/)
* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


