---
title: OdtSaveOptions Class
linktitle: OdtSaveOptions
articleTitle: OdtSaveOptions
second_title: .NET için Aspose.Words
description: Belge kaydetme deneyiminizi geliştirmek için Aspose.Words.OdtSaveOptions'ı keşfedin. ODT/OTT biçimleri için ayarları özelleştirin ve iş akışınızı optimize edin!
type: docs
weight: 6110
url: /tr/net/aspose.words.saving/odtsaveoptions/
---
## OdtSaveOptions class

Bir belgeyi kaydederken ek seçenekleri belirtmek için kullanılabilirOdt veya Ott biçim.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Kaydetme Seçeneklerini Belirleyin](https://docs.aspose.com/words/net/specify-save-options/) belgeleme makalesi.

```csharp
public class OdtSaveOptions : SaveOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [OdtSaveOptions](odtsaveoptions/#constructor)() | Bu sınıfın, bir belgeyi kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Odt biçim. |
| [OdtSaveOptions](odtsaveoptions/#constructor_1)(*[SaveFormat](../../aspose.words/saveformat/)*) | Bu sınıfın, bir belgeyi kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Odt veya Ott biçim. |
| [OdtSaveOptions](odtsaveoptions/#constructor_2)(*string*) | Bu sınıfın, bir belgeyi kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Odt format şifreyle şifrelenmiş. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | PostScript anahatlarıyla yazı tiplerinin gömülmesine izin verilip verilmeyeceğini belirten bir Boole değeri alır veya ayarlar. Bir belge kaydedildiğinde TrueType yazı tiplerini gömerken. Varsayılan değer`YANLIŞ` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Varsayılan şablona giden yolu alır veya ayarlar (dosya adı dahil). Bu özellik için varsayılan değer**boş dize** (Empty ). |
| [DigitalSignatureDetails](../../aspose.words.saving/odtsaveoptions/digitalsignaturedetails/) { get; set; } | Alır veya ayarlar[`DigitalSignatureDetails`](../digitalsignaturedetails/) Bir belgeyi imzalamak için kullanılan nesne. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | 3B efektlerin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | DrawingML efektlerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | DrawingML şekillerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Ne zaman`doğru` , Aspose.Words adının ve sürümünün üretilen dosyalara gömülmesine neden olur. Varsayılan değer`doğru` . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Mürekkep (InkML) nesnelerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [IsStrictSchema11](../../aspose.words.saving/odtsaveoptions/isstrictschema11/) { get; set; } | Dışa aktarma işleminin kesinlikle ODT 1.1 spesifikasyonuna uyup uymayacağını belirtir. OOo 3.0, dosyaları ODT 1.2 öğelerini ve özniteliklerini içerdiğinde doğru şekilde görüntüler. Bu amaçla "false" veya 1.1 spesifikasyonuna kesinlikle uymak için "true" kullanın. Varsayılan değer şudur:`YANLIŞ` . |
| [MeasureUnit](../../aspose.words.saving/odtsaveoptions/measureunit/) { get; set; } | Belge içeriğine uygulanacak ölçü birimlerini belirtmenize olanak tanır. Varsayılan değerCentimeters |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Belgeyi kaydetmeden önce bellek optimizasyonunun yapılıp yapılmayacağını belirleyen değeri alır veya ayarlar. Bu özelliğin varsayılan değeri`YANLIŞ` . |
| [Password](../../aspose.words.saving/odtsaveoptions/password/) { get; set; } | Belgeyi şifrelemek için bir parola alır veya ayarlar. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Ne zaman`doğru` , uygun olduğu durumlarda çıktıyı güzel biçimlerde biçimlendirir. Varsayılan değer`YANLIŞ` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Bir belgeyi kaydederken çağrılır ve kaydetme ilerlemesiyle ilgili verileri kabul eder. |
| override [SaveFormat](../../aspose.words.saving/odtsaveoptions/saveformat/) { get; set; } | Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. Odt veyaOtt . |
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

Kaydedilmiş bir belgenin eski bir ODT şemasına uygun hale getirilmesinin nasıl yapılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

Kaydedilmiş bir ODT belgesinin stil parametrelerini tanımlamak için farklı ölçüm birimlerinin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Belgeyi .odt'ye aktardığımızda, belgeyi nasıl kaydedeceğimizi değiştirmek için OdtSaveOptions nesnesini kullanabiliriz.
// "MeasureUnit" özelliğini "OdtSaveMeasureUnit.Centimeters" olarak ayarlayabiliriz
 // Open Office'in kullandığı metrik sistemi kullanarak stil parametreleri gibi içerikleri tanımlamak için.
// "MeasureUnit" özelliğini "OdtSaveMeasureUnit.Inches" olarak ayarlayabiliriz
// Microsoft Word'ün kullandığı imparatorluk sistemini kullanarak stil parametreleri gibi içerikleri tanımlamak için.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Ayrıca bakınız

* class [SaveOptions](../saveoptions/)
* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
