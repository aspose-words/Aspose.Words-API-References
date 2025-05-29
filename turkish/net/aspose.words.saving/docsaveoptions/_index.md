---
title: DocSaveOptions Class
linktitle: DocSaveOptions
articleTitle: DocSaveOptions
second_title: .NET için Aspose.Words
description: Aspose.Words.Saving.DocSaveOptions ile belge kaydetmeyi optimize edin. Gelişmiş kalite ve esneklik için Doc ve Dot formatlarınızı özelleştirin.
type: docs
weight: 5680
url: /tr/net/aspose.words.saving/docsaveoptions/
---
## DocSaveOptions class

Bir belgeyi kaydederken ek seçenekleri belirtmek için kullanılabilirDoc veya Dot biçim.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Kaydetme Seçeneklerini Belirleyin](https://docs.aspose.com/words/net/specify-save-options/) belgeleme makalesi.

```csharp
public class DocSaveOptions : SaveOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [DocSaveOptions](docsaveoptions/#constructor)() | Bu sınıfın, bir belgeyi kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Doc biçim. |
| [DocSaveOptions](docsaveoptions/#constructor_1)(*[SaveFormat](../../aspose.words/saveformat/)*) | Bu sınıfın, bir belgeyi kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Doc veya Dot biçim. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | PostScript anahatlarıyla yazı tiplerinin gömülmesine izin verilip verilmeyeceğini belirten bir Boole değeri alır veya ayarlar. Bir belge kaydedildiğinde TrueType yazı tiplerini gömerken. Varsayılan değer`YANLIŞ` . |
| [AlwaysCompressMetafiles](../../aspose.words.saving/docsaveoptions/alwayscompressmetafiles/) { get; set; } | Ne zaman`YANLIŞ` , küçük meta dosyaları performans nedeniyle sıkıştırılmaz. Varsayılan değer`doğru` , tüm meta dosyaları boyutuna bakılmaksızın sıkıştırılır. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Varsayılan şablona giden yolu alır veya ayarlar (dosya adı dahil). Bu özellik için varsayılan değer**boş dize** (Empty ). |
| [DigitalSignatureDetails](../../aspose.words.saving/docsaveoptions/digitalsignaturedetails/) { get; set; } | Alır veya ayarlar[`DigitalSignatureDetails`](../digitalsignaturedetails/) Bir belgeyi imzalamak için kullanılan nesne. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | 3B efektlerin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | DrawingML efektlerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | DrawingML şekillerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Ne zaman`doğru` , Aspose.Words adının ve sürümünün üretilen dosyalara gömülmesine neden olur. Varsayılan değer`doğru` . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Mürekkep (InkML) nesnelerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Belgeyi kaydetmeden önce bellek optimizasyonunun yapılıp yapılmayacağını belirleyen değeri alır veya ayarlar. Bu özelliğin varsayılan değeri`YANLIŞ` . |
| [Password](../../aspose.words.saving/docsaveoptions/password/) { get; set; } | Belgeyi RC4 şifreleme yöntemini kullanarak şifrelemek için bir parola alır/ayarlar. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Ne zaman`doğru` , uygun olduğu durumlarda çıktıyı güzel biçimlerde biçimlendirir. Varsayılan değer`YANLIŞ` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Bir belgeyi kaydederken çağrılır ve kaydetme ilerlemesiyle ilgili verileri kabul eder. |
| override [SaveFormat](../../aspose.words.saving/docsaveoptions/saveformat/) { get; set; } | Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. Doc veyaDot . |
| [SavePictureBullet](../../aspose.words.saving/docsaveoptions/savepicturebullet/) { get; set; } | Ne zaman`YANLIŞ` , PictureBullet verileri çıktı belgesine kaydedilmez. Varsayılan değer`doğru` . |
| [SaveRoutingSlip](../../aspose.words.saving/docsaveoptions/saveroutingslip/) { get; set; } | Ne zaman`YANLIŞ` , RoutingSlip verileri çıktı belgesine kaydedilmez. Varsayılan değer`doğru` . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik`hükümsüz` ve geçici dosyalar kullanılmaz. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Kullanılan karakter koduna göre yazı tipi özniteliklerinin değiştirilip değiştirilmeyeceğini belirler. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Bir değeri alır veya ayarlar.[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) özellik kaydedilmeden önce güncellenir. Varsayılan değer`YANLIŞ` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Belgeyi sabit bir sayfa biçimine kaydetmeden önce belirli türdeki alanların güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. Bu özelliğin varsayılan değeri`doğru` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Bir değeri alır veya ayarlar.[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) özellik kaydedilmeden önce güncellenir. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Bir değeri alır veya ayarlar.[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) özellik kaydedilmeden önce güncellenir. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | İşleme için kenar yumuşatma kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Yüksek kaliteli (yani yavaş) işleme algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar. |

## Notlar

Şu anda yalnızca şunu sağlar:[`SaveFormat`](./saveformat/) özelliği, ancak gelecekte şifreleme parolası veya dijital imza ayarları gibi diğer seçenekler eklenecek.

## Örnekler

Eski Microsoft Word biçimleri için kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Microsoft Word veya Aspose.Words ile belgenin yüklenmesini koruyacak bir parola belirleyin.
// Bu işlemin belgenin içeriğini hiçbir şekilde şifrelemediğini unutmayın.
options.Password = "MyPassword";

// Belgede yönlendirme fişi varsa, bu bayrağı true olarak ayarlayarak kaydederken bunu koruyabiliriz.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// Belgeyi yükleyebilmek için,
// DocSaveOptions nesnesinde belirttiğimiz şifreyi bir LoadOptions nesnesine uygulamamız gerekecek.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [SaveOptions](../saveoptions/)
* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
