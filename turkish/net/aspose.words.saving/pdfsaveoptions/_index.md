---
title: PdfSaveOptions Class
linktitle: PdfSaveOptions
articleTitle: PdfSaveOptions
second_title: .NET için Aspose.Words
description: Belge kaydetme deneyiminizi geliştirmek için Aspose.Words.PdfSaveOptions'ı keşfedin. En iyi PDF çıktı kalitesi ve performansı için ayarları özelleştirin.
type: docs
weight: 6320
url: /tr/net/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class

Bir belgeyi kaydederken ek seçenekleri belirtmek için kullanılabilirPdf biçim.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Kaydetme Seçeneklerini Belirleyin](https://docs.aspose.com/words/net/specify-save-options/) belgeleme makalesi.

```csharp
public class PdfSaveOptions : FixedPageSaveOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [PdfSaveOptions](pdfsaveoptions/)() | Bu sınıfın, içindeki bir belgeyi kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Pdf biçim. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AdditionalTextPositioning](../../aspose.words.saving/pdfsaveoptions/additionaltextpositioning/) { get; set; } | Ek metin konumlandırma operatörlerinin yazılıp yazılamayacağını belirten bir bayrak. |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | PostScript anahatlarıyla yazı tiplerinin gömülmesine izin verilip verilmeyeceğini belirten bir Boole değeri alır veya ayarlar. Bir belge kaydedildiğinde TrueType yazı tiplerini gömerken. Varsayılan değer`YANLIŞ` . |
| [AttachmentsEmbeddingMode](../../aspose.words.saving/pdfsaveoptions/attachmentsembeddingmode/) { get; set; } | Eklerin PDF belgesine nasıl yerleştirileceğini belirleyen bir değer alır veya ayarlar. |
| [CacheBackgroundGraphics](../../aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/) { get; set; } | Belgenin arka planına yerleştirilen grafiklerin önbelleğe alınıp alınmayacağını belirleyen bir değer alır veya ayarlar. |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Renklerin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [Compliance](../../aspose.words.saving/pdfsaveoptions/compliance/) { get; set; } | Çıktı belgeleri için PDF standartlarına uyumluluk düzeyini belirtir. |
| [CreateNoteHyperlinks](../../aspose.words.saving/pdfsaveoptions/createnotehyperlinks/) { get; set; } | Ana metin öyküsündeki dipnot/sonnot referanslarının etkin köprü metinlerine dönüştürülüp dönüştürülmeyeceğini belirtir. Köprü metni tıklandığında ilgili dipnot/sonnot'a yönlendirilir. Varsayılan`YANLIŞ` . |
| [CustomPropertiesExport](../../aspose.words.saving/pdfsaveoptions/custompropertiesexport/) { get; set; } | Yolu belirleyen bir değer alır veya ayarlar[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) PDF dosyasına aktarılır. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Varsayılan şablona giden yolu alır veya ayarlar (dosya adı dahil). Bu özellik için varsayılan değer**boş dize** (Empty ). |
| [DigitalSignatureDetails](../../aspose.words.saving/pdfsaveoptions/digitalsignaturedetails/) { get; set; } | Çıktı PDF belgesinin imzalanması için ayrıntıları alır veya ayarlar. |
| [DisplayDocTitle](../../aspose.words.saving/pdfsaveoptions/displaydoctitle/) { get; set; } | Pencerenin başlık çubuğunun, belge bilgi sözlüğünün Başlık girişinden alınan belge başlığını görüntüleyip görüntülemeyeceğini belirten bir bayrak. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | 3B efektlerin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| override [DmlEffectsRenderingMode](../../aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode/) { get; set; } | DrawingML efektlerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | DrawingML şekillerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [DownsampleOptions](../../aspose.words.saving/pdfsaveoptions/downsampleoptions/) { get; set; } | Alt örnekleme seçeneklerini belirtmeye izin verir. |
| [EmbedFullFonts](../../aspose.words.saving/pdfsaveoptions/embedfullfonts/) { get; set; } | Yazı tiplerinin ortaya çıkan PDF belgelerine nasıl yerleştirileceğini kontrol eder. |
| [EncryptionDetails](../../aspose.words.saving/pdfsaveoptions/encryptiondetails/) { get; set; } | Çıktı PDF belgesinin şifrelenmesine ilişkin ayrıntıları alır veya ayarlar. |
| [ExportDocumentStructure](../../aspose.words.saving/pdfsaveoptions/exportdocumentstructure/) { get; set; } | Belge yapısının dışa aktarılıp aktarılmayacağını belirleyen bir değer alır veya ayarlar. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Ne zaman`doğru` , Aspose.Words adının ve sürümünün üretilen dosyalara gömülmesine neden olur. Varsayılan değer`doğru` . |
| [ExportLanguageToSpanTag](../../aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/) { get; set; } | Metin dilini dışa aktarmak için belge yapısında bir "Span" etiketi oluşturulup oluşturulmayacağını belirleyen bir değer alır veya ayarlar. |
| [ExportParagraphGraphicsToArtifact](../../aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/) { get; set; } | Bir paragraf grafiğinin bir yapıt olarak işaretlenip işaretlenmeyeceğini belirleyen bir değeri alır veya ayarlar. |
| [FontEmbeddingMode](../../aspose.words.saving/pdfsaveoptions/fontembeddingmode/) { get; set; } | Yazı tipi yerleştirme modunu belirtir. |
| [HeaderFooterBookmarksExportMode](../../aspose.words.saving/pdfsaveoptions/headerfooterbookmarksexportmode/) { get; set; } | Başlıklar/altbilgilerdeki yer imlerinin nasıl dışa aktarılacağını belirler. |
| [ImageColorSpaceExportMode](../../aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/) { get; set; } | PDF belgesindeki resimler için renk alanının nasıl seçileceğini belirtir. |
| [ImageCompression](../../aspose.words.saving/pdfsaveoptions/imagecompression/) { get; set; } | Belgedeki tüm görüntüler için kullanılacak sıkıştırma türünü belirtir. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Mürekkep (InkML) nesnelerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [InterpolateImages](../../aspose.words.saving/pdfsaveoptions/interpolateimages/) { get; set; } | Görüntü enterpolasyonunun uygun bir okuyucu tarafından yapılıp yapılmayacağını belirten bir bayrak. Ne zaman`YANLIŞ` belirtildiğinde, bayrak çıktı belgesine yazılmaz ve bunun yerine okuyucunun varsayılan davranışı kullanılır. |
| [JpegQuality](../../aspose.words.saving/pdfsaveoptions/jpegquality/) { get; set; } | PDF belgesinin içindeki JPEG görüntülerinin kalitesini belirleyen bir değeri alır veya ayarlar. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Belgeyi kaydetmeden önce bellek optimizasyonunun yapılıp yapılmayacağını belirleyen değeri alır veya ayarlar. Bu özelliğin varsayılan değeri`YANLIŞ` . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Meta dosyası oluşturma seçeneklerini belirtmenize olanak tanır. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Alır veya ayarlar[`NumeralFormat`](../numeralformat/) rakamların işlenmesi için kullanılır. Varsayılan olarak Avrupa rakamları kullanılır. |
| [OpenHyperlinksInNewWindow](../../aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/) { get; set; } | Çıktı Pdf belgesindeki köprü metinlerinin bir tarayıcının yeni bir penceresinde (veya sekmesinde) açılmasının zorunlu olup olmadığını belirleyen bir değer alır veya ayarlar. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | Bayrağı, çıktının optimize edilmesinin gerekip gerekmediğini belirtir. Bu bayrak ayarlanırsa, gereksiz iç içe geçmiş tuvaller ve boş tuvaller kaldırılır, aynı biçimlendirmeye sahip komşu glifler de birleştirilir. Not: Bu özellik olarak ayarlanırsa içerik görüntüsünün doğruluğu etkilenebilir.`doğru` . Varsayılan`YANLIŞ` . |
| [OutlineOptions](../../aspose.words.saving/pdfsaveoptions/outlineoptions/) { get; } | Anahat seçeneklerini belirtmenize olanak tanır. |
| [PageLayout](../../aspose.words.saving/pdfsaveoptions/pagelayout/) { get; set; } | Belge bir PDF okuyucusunda açıldığında kullanılacak sayfa düzenini belirtir. |
| [PageMode](../../aspose.words.saving/pdfsaveoptions/pagemode/) { get; set; } | PDF belgesinin bir PDF okuyucusunda açıldığında nasıl görüntüleneceğini belirtir. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Bir belge sabit sayfa biçimine aktarıldığında ayrı sayfaların nasıl kaydedileceğini kontrol etmenizi sağlar. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | İşlenecek sayfaları alır veya ayarlar. Varsayılan, belgedeki tüm sayfalardır. |
| [PreblendImages](../../aspose.words.saving/pdfsaveoptions/preblendimages/) { get; set; } | Şeffaf resimlerin siyah arka plan rengiyle önceden karıştırılıp karıştırılmayacağını belirleyen bir değer alır veya ayarlar. |
| [PreserveFormFields](../../aspose.words.saving/pdfsaveoptions/preserveformfields/) { get; set; } | Microsoft Word form alanlarının PDF'de form alanları olarak korunacağını veya metne dönüştürüleceğini belirtir. Varsayılan`YANLIŞ` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Ne zaman`doğru` , uygun olduğu durumlarda çıktıyı güzel biçimlerde biçimlendirir. Varsayılan değer`YANLIŞ` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Bir belgeyi kaydederken çağrılır ve kaydetme ilerlemesiyle ilgili verileri kabul eder. |
| [RenderChoiceFormFieldBorder](../../aspose.words.saving/pdfsaveoptions/renderchoiceformfieldborder/) { get; set; } | PDF seçim formu alanı kenarlığının işlenip işlenmeyeceğini belirtir. |
| override [SaveFormat](../../aspose.words.saving/pdfsaveoptions/saveformat/) { get; set; } | Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. YalnızcaPdf . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik`hükümsüz` ve geçici dosyalar kullanılmaz. |
| [TextCompression](../../aspose.words.saving/pdfsaveoptions/textcompression/) { get; set; } | Belgedeki tüm metinsel içerik için kullanılacak sıkıştırma türünü belirtir. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Kullanılan karakter koduna göre yazı tipi özniteliklerinin değiştirilip değiştirilmeyeceğini belirler. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Bir değeri alır veya ayarlar.[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) özellik kaydedilmeden önce güncellenir. Varsayılan değer`YANLIŞ` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Belgeyi sabit bir sayfa biçimine kaydetmeden önce belirli türdeki alanların güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. Bu özelliğin varsayılan değeri`doğru` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Bir değeri alır veya ayarlar.[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) özellik kaydedilmeden önce güncellenir. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Bir değeri alır veya ayarlar.[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) özellik kaydedilmeden önce güncellenir. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | İşleme için kenar yumuşatma kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |
| [UseBookFoldPrintingSettings](../../aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/) { get; set; } | Belgenin kitapçık yazdırma düzeni kullanılarak kaydedilip kaydedilmeyeceğini belirten bir Boole değeri alır veya ayarlar, bu şekilde belirtilmişse[`MultiplePages`](../../aspose.words/pagesetup/multiplepages/) . |
| [UseCoreFonts](../../aspose.words.saving/pdfsaveoptions/usecorefonts/) { get; set; } | TrueType yazı tipleri Arial, Times New Roman, Courier New ve Symbol'ün çekirdek PDF Type 1 yazı tipleriyle değiştirilip değiştirilmeyeceğini belirleyen bir değer alır veya ayarlar. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Yüksek kaliteli (yani yavaş) işleme algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar. |
| [UseSdtTagAsFormFieldName](../../aspose.words.saving/pdfsaveoptions/usesdttagasformfieldname/) { get; set; } | PDF'deki form alanının adı olarak SDT denetim Etiketi veya Kimlik özelliğinin kullanılıp kullanılmayacağını belirtir. |
| [ZoomBehavior](../../aspose.words.saving/pdfsaveoptions/zoombehavior/) { get; set; } | Bir belge PDF görüntüleyicisiyle açıldığında hangi tür yakınlaştırmanın uygulanacağını belirleyen bir değer alır veya ayarlar. |
| [ZoomFactor](../../aspose.words.saving/pdfsaveoptions/zoomfactor/) { get; set; } | Bir belge için yakınlaştırma faktörünü (yüzde olarak) belirleyen bir değer alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clone](../../aspose.words.saving/pdfsaveoptions/clone/)() | Bu nesnenin derin bir klonunu oluşturur. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(*object*) | Belirtilen nesnenin geçerli nesneye eşit değerde olup olmadığını belirler. |

## Örnekler

Resim renginin kaydetme seçenekleri özelliği ile nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
// Belgedeki tüm görselleri siyah beyaz yapmak için "ColorMode" özelliğini "Gri Tonlamalı" olarak ayarlayın.
// Bu ayarla çıktı belgesinin boyutu daha büyük olabilir.
// Tüm görselleri renkli hale getirmek için "ColorMode" özelliğini "Normal" olarak ayarlayın.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

Bir belgeyi PDF'e kaydederken metin sıkıştırmanın nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Herhangi bir uygulama yapmamak için "TextCompression" özelliğini "PdfTextCompression.None" olarak ayarlayın
// Belgeyi PDF'e kaydettiğimizde metne sıkıştırma.
// ZIP sıkıştırmasını uygulamak için "TextCompression" özelliğini "PdfTextCompression.Flate" olarak ayarlayın
// Belgeyi PDF'e kaydettiğimizde metne. Belge ne kadar büyükse, bunun etkisi de o kadar büyük olacaktır.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

Belgenin tamamının üç düzeyde PDF'ye nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 1'den 5'e kadar olan seviyelerin başlıklarını ekleyin.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Çıktı PDF belgesi, belge gövdesindeki başlıkları listeleyen bir içerik tablosu olan bir ana hat içerecektir.
// Bu taslaktaki bir girdiye tıkladığımızda ilgili başlığın bulunduğu yere gideceğiz.
// Anahattan 4'ün üstündeki tüm başlıkları hariç tutmak için "HeadingsOutlineLevels" özelliğini "4" olarak ayarlayın.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Bir ana hat girişinin kendisi ile aynı veya daha düşük seviyedeki bir sonraki giriş arasında daha yüksek seviyede müteakip girişler varsa,
// girişin solunda bir ok belirecektir. Bu giriş, bu tür birkaç "alt girişin" "sahibi"dir.
// Belgemizde, 5. başlık seviyesindeki ana hat girişleri, ikinci 4. seviye ana hat girişinin alt girişleridir.
// 4. ve 5. başlık seviyesi girişleri, 2. 3. seviye girişin alt girişleridir, vb.
// Anahatta, "sahip" girişinin okuna tıklayarak tüm alt girişlerini daraltabilir/genişletebiliriz.
// Tüm başlık düzeyi 2 ve alt anahat girişlerini otomatik olarak genişletmek için "ExpandedOutlineLevels" özelliğini "2" olarak ayarlayın
// ve belgeyi açtığımızda tüm seviye ve 3 ve üzeri girdileri daraltırız.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Ayrıca bakınız

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
