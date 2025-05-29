---
title: OoxmlSaveOptions Class
linktitle: OoxmlSaveOptions
articleTitle: OoxmlSaveOptions
second_title: .NET için Aspose.Words
description: Özelleştirilebilir özelliklerle Docx, Docm, Dotx, Dotm ve FlatOpc formatlarındaki belge kaydetmeyi geliştirmek için Aspose.Words.OoxmlSaveOptions'ı keşfedin.
type: docs
weight: 6130
url: /tr/net/aspose.words.saving/ooxmlsaveoptions/
---
## OoxmlSaveOptions class

Bir belgeyi kaydederken ek seçenekleri belirtmek için kullanılabilirDocx , Docm ,Dotx ,Dotm veya FlatOpc biçim.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Kaydetme Seçeneklerini Belirleyin](https://docs.aspose.com/words/net/specify-save-options/) belgeleme makalesi.

```csharp
public class OoxmlSaveOptions : SaveOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [OoxmlSaveOptions](ooxmlsaveoptions/#constructor)() | Bu sınıfın, bir belgeyi kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Docx biçim. |
| [OoxmlSaveOptions](ooxmlsaveoptions/#constructor_1)(*[SaveFormat](../../aspose.words/saveformat/)*) | Bu sınıfın, bir belgeyi kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Docx , Docm ,Dotx ,Dotm veya FlatOpc biçim. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | PostScript anahatlarıyla yazı tiplerinin gömülmesine izin verilip verilmeyeceğini belirten bir Boole değeri alır veya ayarlar. Bir belge kaydedildiğinde TrueType yazı tiplerini gömerken. Varsayılan değer`YANLIŞ` . |
| [Compliance](../../aspose.words.saving/ooxmlsaveoptions/compliance/) { get; set; } | Çıktı belgesi için OOXML sürümünü belirtir. Varsayılan değerEcma376_2006 . |
| [CompressionLevel](../../aspose.words.saving/ooxmlsaveoptions/compressionlevel/) { get; set; } | Belgeyi kaydetmek için kullanılan sıkıştırma düzeyini belirtir. Varsayılan değerNormal . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Varsayılan şablona giden yolu alır veya ayarlar (dosya adı dahil). Bu özellik için varsayılan değer**boş dize** (Empty ). |
| [DigitalSignatureDetails](../../aspose.words.saving/ooxmlsaveoptions/digitalsignaturedetails/) { get; set; } | Alır veya ayarlar[`DigitalSignatureDetails`](../digitalsignaturedetails/) Bir belgeyi imzalamak için kullanılan nesne. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | 3B efektlerin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | DrawingML efektlerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | DrawingML şekillerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Ne zaman`doğru` , Aspose.Words adının ve sürümünün üretilen dosyalara gömülmesine neden olur. Varsayılan değer`doğru` . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Mürekkep (InkML) nesnelerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [KeepLegacyControlChars](../../aspose.words.saving/ooxmlsaveoptions/keeplegacycontrolchars/) { get; set; } | Eski kontrol karakterlerinin orijinal gösterimini korur. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Belgeyi kaydetmeden önce bellek optimizasyonunun yapılıp yapılmayacağını belirleyen değeri alır veya ayarlar. Bu özelliğin varsayılan değeri`YANLIŞ` . |
| [Password](../../aspose.words.saving/ooxmlsaveoptions/password/) { get; set; } | ECMA376 Standart şifreleme algoritmasını kullanarak belgeyi şifrelemek için bir parola alır/ayarlar. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Ne zaman`doğru` , uygun olduğu durumlarda çıktıyı güzel biçimlerde biçimlendirir. Varsayılan değer`YANLIŞ` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Bir belgeyi kaydederken çağrılır ve kaydetme ilerlemesiyle ilgili verileri kabul eder. |
| override [SaveFormat](../../aspose.words.saving/ooxmlsaveoptions/saveformat/) { get; set; } | Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. Docx ,Docm , Dotx ,Dotm veyaFlatOpc . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik`hükümsüz` ve geçici dosyalar kullanılmaz. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Kullanılan karakter koduna göre yazı tipi özniteliklerinin değiştirilip değiştirilmeyeceğini belirler. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Bir değeri alır veya ayarlar.[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) özellik kaydedilmeden önce güncellenir. Varsayılan değer`YANLIŞ` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Belgeyi sabit bir sayfa biçimine kaydetmeden önce belirli türdeki alanların güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. Bu özelliğin varsayılan değeri`doğru` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Bir değeri alır veya ayarlar.[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) özellik kaydedilmeden önce güncellenir. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Bir değeri alır veya ayarlar.[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) özellik kaydedilmeden önce güncellenir. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | İşleme için kenar yumuşatma kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Yüksek kaliteli (yani yavaş) işleme algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar. |
| [Zip64Mode](../../aspose.words.saving/ooxmlsaveoptions/zip64mode/) { get; set; } | Çıktı belgesi için ZIP64 biçim uzantılarının kullanılıp kullanılmayacağını belirtir. Varsayılan değer:Never . |

## Örnekler

Kaydedilen bir belgenin uyması gereken OOXML uyumluluk spesifikasyonunun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Uyumluluk seçeneklerini Microsoft Word 2003 ile uyumlu olacak şekilde yapılandırırsak,
// Bir resim eklemek, VML kullanılarak şeklinin tanımlanmasını sağlayacaktır.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// "ISO/IEC 29500:2008" OOXML standardı VML şekillerini desteklemez.
// SaveOptions nesnesinin "Compliance" özelliğini "OoxmlCompliance.Iso29500_2008_Strict" olarak ayarlarsak,
 // Bu nesneyi geçirirken kaydettiğimiz her belgenin o standarda uyması gerekecektir.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Kaydedilen belgemiz, "ISO/IEC 29500:2008" OOXML standardına uymak için şekli DML kullanarak tanımlar.
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### Ayrıca bakınız

* class [SaveOptions](../saveoptions/)
* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
