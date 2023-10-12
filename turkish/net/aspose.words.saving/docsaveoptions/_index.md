---
title: Class DocSaveOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.DocSaveOptions sınıf. Bir belgeyi bilgisayara kaydederken ek seçenekleri belirlemek için kullanılabilir.Doc veya Dot format.
type: docs
weight: 4930
url: /tr/net/aspose.words.saving/docsaveoptions/
---
## DocSaveOptions class

Bir belgeyi bilgisayara kaydederken ek seçenekleri belirlemek için kullanılabilir.Doc veya Dot format.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Kaydetme Seçeneklerini Belirtin](https://docs.aspose.com/words/net/specify-save-options/) dokümantasyon makalesi.

```csharp
public class DocSaveOptions : SaveOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [DocSaveOptions](docsaveoptions/#constructor)() | Bir belgeyi kaydetmek için kullanılabilecek bu sınıfın yeni bir örneğini başlatır.Doc format. |
| [DocSaveOptions](docsaveoptions/#constructor_1)(SaveFormat) | Bir belgeyi kaydetmek için kullanılabilecek bu sınıfın yeni bir örneğini başlatır.Doc veya Dot format. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Kaydedildikten sonra TrueType yazı tiplerini bir belgeye gömerken PostScript ana hatlarıyla yazı tiplerinin gömülmesine izin verilip verilmeyeceğini belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`YANLIŞ` . |
| [AlwaysCompressMetafiles](../../aspose.words.saving/docsaveoptions/alwayscompressmetafiles/) { get; set; } | Ne zaman`YANLIŞ` , küçük meta dosyalar performans nedeniyle sıkıştırılmaz. Varsayılan değer:`doğru` , tüm meta dosyalar boyutuna bakılmaksızın sıkıştırılır. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Varsayılan şablonun yolunu alır veya ayarlar (dosya adı dahil). Bu özellik için varsayılan değer: **boş dize** (Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | 3B efektlerin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | DrawingML efektlerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | DrawingML şekillerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Ne zaman`doğru` , Aspose.Words'ün adının ve sürümünün üretilen dosyalara yerleştirilmesine neden olur. Varsayılan değer:`doğru` . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Mürekkep (InkML) nesnelerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Belgeyi kaydetmeden önce bellek optimizasyonunun gerçekleştirilip gerçekleştirilmeyeceğini belirleyen değeri alır veya ayarlar. Bu özellik için varsayılan değer:`YANLIŞ` . |
| [Password](../../aspose.words.saving/docsaveoptions/password/) { get; set; } | Belgeyi RC4 şifreleme yöntemini kullanarak şifrelemek için bir parola alır/ayarlar. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Ne zaman`doğru` uygulanabilir olduğu yerde güzel formatlarda çıktı. Varsayılan değer:`YANLIŞ` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Bir belge kaydedilirken çağrılır ve kaydetme işlemiyle ilgili verileri kabul eder. |
| override [SaveFormat](../../aspose.words.saving/docsaveoptions/saveformat/) { get; set; } | Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. OlabilirDoc veyaDot . |
| [SavePictureBullet](../../aspose.words.saving/docsaveoptions/savepicturebullet/) { get; set; } | Ne zaman`YANLIŞ` , PictureBullet verileri çıktı belgesine kaydedilmez. Varsayılan değer:`doğru` . |
| [SaveRoutingSlip](../../aspose.words.saving/docsaveoptions/saveroutingslip/) { get; set; } | Ne zaman`YANLIŞ` , RoutingSlip verileri çıktı belgesine kaydedilmez. Varsayılan değer:`doğru` . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Bir DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik`hükümsüz` ve hiçbir geçici dosya kullanılmaz. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Bir değer alır veya ayarlar.[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) özellik kaydedilmeden önce güncellenir. Varsayılan değer:`YANLIŞ` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Belgeyi sabit bir sayfa formatında kaydetmeden önce belirli türlerdeki alanların güncellenmesi gerekip gerekmediğini belirleyen bir değer alır veya ayarlar. Bu özellik için varsayılan değer:`doğru` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Bir değer alır veya ayarlar.[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) özellik kaydedilmeden önce güncellenir. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Bir değer alır veya ayarlar.[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) özellik kaydedilmeden önce güncellenir. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Oluşturma için kenar yumuşatma kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Yüksek kaliteli (yani yavaş) oluşturma algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |

### Notlar

Şu anda yalnızca şunları sağlıyor:[`SaveFormat`](./saveformat/) özelliğidir, ancak gelecekte şifreleme parolası veya dijital imza ayarları gibi başka seçenekler de eklenecektir.

### Örnekler

Eski Microsoft Word formatları için kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Belgenin Microsoft Word veya Aspose.Words tarafından yüklenmesini koruyacak bir şifre belirleyin.
// Bunun belgenin içeriğini hiçbir şekilde şifrelemediğini unutmayın.
options.Password = "MyPassword";

// Doküman bir yönlendirme fişi içeriyorsa bu bayrağı true yaparak kaydederken onu koruyabiliriz.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// Dokümanı yükleyebilmek için,
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


