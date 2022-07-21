---
title: DocSaveOptions
second_title: Aspose.Words for .NET API Referansı
description: Bir belgeyi dosyaya kaydederken ek seçenekleri belirtmek için kullanılabilir.Doc or Dot biçim.
type: docs
weight: 4670
url: /tr/net/aspose.words.saving/docsaveoptions/
---
## DocSaveOptions class

Bir belgeyi dosyaya kaydederken ek seçenekleri belirtmek için kullanılabilir.Doc or Dot biçim.

```csharp
public class DocSaveOptions : SaveOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [DocSaveOptions](docsaveoptions#constructor)() | Dosyaya bir belgeyi kaydetmek için kullanılabilecek bu sınıfın yeni bir örneğini başlatır.Doc biçim. |
| [DocSaveOptions](docsaveoptions#constructor_1)(SaveFormat) | Dosyaya bir belgeyi kaydetmek için kullanılabilecek bu sınıfın yeni bir örneğini başlatır.Doc or Dot biçim. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | TrueType yazı tiplerini bir belgeye gömerken PostScript anahatlarıyla yazı tiplerinin gömülmesine izin verilip verilmeyeceğini belirten bir boole değeri alır veya ayarlar. Varsayılan değer şudur: **yanlış** . |
| [AlwaysCompressMetafiles](../../aspose.words.saving/docsaveoptions/alwayscompressmetafiles) { get; set; } | Ne zaman`yanlış` , küçük meta dosyaları performans nedeniyle sıkıştırılmaz. Varsayılan değer **doğru** , boyutundan bağımsız olarak tüm meta dosyaları sıkıştırılır. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | Varsayılan şablonun yolunu alır veya ayarlar (dosya adı dahil). Bu özellik için varsayılan değer **boş dize** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | 3B efektlerin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | DrawingML efektlerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | DrawingML şekillerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | Doğru olduğunda, Aspose.Words'ün adının ve sürümünün üretilen dosyalara gömülmesine neden olur. Varsayılan değerdir **doğru** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | Hangi belge biçimlerinin eşlenmesine izin verildiğini belirleyen değeri alır veya ayarlar.[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . Yalnızca varsayılan olarakFlatOpc belge biçiminin eşlenmesine izin verilir. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | Mürekkep (InkML) nesnelerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | Belgeyi kaydetmeden önce bellek optimizasyonunun yapılıp yapılmayacağını belirleyen değeri alır veya ayarlar. Bu özellik için varsayılan değer **yanlış** . |
| [Password](../../aspose.words.saving/docsaveoptions/password) { get; set; } | Belgeyi RC4 şifreleme yöntemini kullanarak şifrelemek için bir parola alır/ayarlar. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | Ne zaman`doğru` , uygun olduğunda güzel biçimler çıktısı. Varsayılan değer **yanlış** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | Bir belge kaydedilirken çağrılır ve ilerleme kaydetmeyle ilgili verileri kabul eder. |
| override [SaveFormat](../../aspose.words.saving/docsaveoptions/saveformat) { get; set; } | Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği formatı belirtir. Doc veyaDot . |
| [SavePictureBullet](../../aspose.words.saving/docsaveoptions/savepicturebullet) { get; set; } | Ne zaman`yanlış` , PictureBullet verileri çıktı belgesine kaydedilmez. Varsayılan değer **doğru** . |
| [SaveRoutingSlip](../../aspose.words.saving/docsaveoptions/saveroutingslip) { get; set; } | Ne zaman`yanlış` , RoutingSlip verileri çıktı belgesine kaydedilmez. Varsayılan değer **doğru** . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | Bir DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik`hükümsüz` ve hiçbir geçici dosya kullanılmaz. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | olup olmadığını belirleyen bir değer alır veya ayarlar.[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime) özellik kaydedilmeden önce güncellenir. Varsayılan değer false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | Belgeyi sabit bir sayfa biçimine kaydetmeden önce belirli türlerdeki alanların güncellenmesi gerekip gerekmediğini belirleyen bir değer alır veya ayarlar. Bu özellik için varsayılan değer **doğru** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | olup olmadığını belirleyen bir değer alır veya ayarlar.[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted) özellik kaydedilmeden önce güncellenir. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | olup olmadığını belirleyen bir değer alır veya ayarlar.[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime) özellik kaydedilmeden önce güncellenir. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | İçeriğin olup olmadığını belirleyen değeri alır veya ayarlar.[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag) kaydetmeden önce güncellenir. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | İşleme için kenar yumuşatma kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | Yüksek kaliteli (yani yavaş) işleme algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |

### Notlar

Şu anda sadece sağlar[`SaveFormat`](./saveformat) ancak gelecekte şifreleme parolası veya dijital imza ayarları gibi başka seçenekler eklenecektir.

### Örnekler

Daha eski Microsoft Word biçimleri için kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Belgenin Microsoft Word veya Aspose.Words tarafından yüklenmesini koruyacak bir şifre belirleyin.
// Bunun belgenin içeriğini hiçbir şekilde şifrelemediğini unutmayın.
options.Password = "MyPassword";

// Belge bir yönlendirme fişi içeriyorsa, bu bayrağı true olarak ayarlayarak kaydederken koruyabiliriz.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// Belgeyi yükleyebilmek için,
// DocSaveOptions nesnesinde belirttiğimiz parolayı bir LoadOptions nesnesinde uygulamamız gerekecek.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [SaveOptions](../saveoptions)
* ad alanı [Aspose.Words.Saving](../../aspose.words.saving)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
