---
title: HtmlFixedSaveOptions Class
linktitle: HtmlFixedSaveOptions
articleTitle: HtmlFixedSaveOptions
second_title: .NET için Aspose.Words
description: Belge kaydetme deneyiminizi geliştirmek için Aspose.Words.Saving.HtmlFixedSaveOptions'ı keşfedin. En iyi HtmlFixed biçim çıktısı için ayarları özelleştirin.
type: docs
weight: 5830
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/
---
## HtmlFixedSaveOptions class

Bir belgeyi kaydederken ek seçenekleri belirtmek için kullanılabilirHtmlFixed biçim.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Kaydetme Seçeneklerini Belirleyin](https://docs.aspose.com/words/net/specify-save-options/) belgeleme makalesi.

```csharp
public class HtmlFixedSaveOptions : FixedPageSaveOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [HtmlFixedSaveOptions](htmlfixedsaveoptions/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | PostScript anahatlarıyla yazı tiplerinin gömülmesine izin verilip verilmeyeceğini belirten bir Boole değeri alır veya ayarlar. Bir belge kaydedildiğinde TrueType yazı tiplerini gömerken. Varsayılan değer`YANLIŞ` . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Renklerin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [CssClassNamesPrefix](../../aspose.words.saving/htmlfixedsaveoptions/cssclassnamesprefix/) { get; set; } | style.css dosyasındaki tüm sınıf adlarına eklenen öneki belirtir. Varsayılan değer`"ah"` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Varsayılan şablona giden yolu alır veya ayarlar (dosya adı dahil). Bu özellik için varsayılan değer**boş dize** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | 3B efektlerin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | DrawingML efektlerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | DrawingML şekillerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [Encoding](../../aspose.words.saving/htmlfixedsaveoptions/encoding/) { get; set; } | HTML'ye aktarırken kullanılacak kodlamayı belirtir. Varsayılan değer`yeni UTF8Kodlama(true)` (BOM ile UTF-8). |
| [ExportEmbeddedCss](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss/) { get; set; } | CSS'nin (Basamaklı Stil Sayfası) Html belgesine yerleştirilip yerleştirilmeyeceğini belirtir. |
| [ExportEmbeddedFonts](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedfonts/) { get; set; } | Yazı tiplerinin Base64 biçiminde Html belgesine gömülmesi gerekip gerekmediğini belirtir. Bu bayrağı ayarlamanın çıktı Html dosyasının boyutunu önemli ölçüde artırabileceğini unutmayın. |
| [ExportEmbeddedImages](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages/) { get; set; } | Görüntülerin Html belgesine Base64 biçiminde gömülmesi gerekip gerekmediğini belirtir. Bu bayrağı ayarlamanın çıktı Html dosyasının boyutunu önemli ölçüde artırabileceğini unutmayın. |
| [ExportEmbeddedSvg](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/) { get; set; } | SVG kaynaklarının Html belgesine gömülüp gömülmeyeceğini belirtir. Varsayılan değer`doğru` . |
| [ExportFormFields](../../aspose.words.saving/htmlfixedsaveoptions/exportformfields/) { get; set; } | Form alanlarının metne veya grafiğe dönüştürülmek yerine interactive öğeleri ('giriş' etiketi olarak) olarak dışa aktarılıp aktarılmayacağına ilişkin göstergeyi alır veya ayarlar. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Ne zaman`doğru` , Aspose.Words adının ve sürümünün üretilen dosyalara gömülmesine neden olur. Varsayılan değer`doğru` . |
| [FontFormat](../../aspose.words.saving/htmlfixedsaveoptions/fontformat/) { get; set; } | Alır veya ayarlar[`ExportFontFormat`](../exportfontformat/) yazı tipi dışa aktarımı için kullanılır. Varsayılan değerWoff . |
| [IdPrefix](../../aspose.words.saving/htmlfixedsaveoptions/idprefix/) { get; set; } | Çıktı belgesindeki tüm oluşturulan öğe kimliklerine eklenen bir önek belirtir. Varsayılan değer null'dır ve hiçbir önek eklenmez. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Mürekkep (InkML) nesnelerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality/) { get; set; } | Html belgesinin içindeki JPEG görüntülerinin kalitesini belirleyen bir değeri alır veya ayarlar. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Belgeyi kaydetmeden önce bellek optimizasyonunun yapılıp yapılmayacağını belirleyen değeri alır veya ayarlar. Bu özelliğin varsayılan değeri`YANLIŞ` . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Meta dosyası oluşturma seçeneklerini belirtmenize olanak tanır. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Alır veya ayarlar[`NumeralFormat`](../numeralformat/) rakamların işlenmesi için kullanılır. Varsayılan olarak Avrupa rakamları kullanılır. |
| override [OptimizeOutput](../../aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/) { get; set; } | Bayrağı, çıktının optimize edilmesinin gerekip gerekmediğini belirtir. Bu bayrak ayarlanırsa, gereksiz iç içe geçmiş tuvaller ve boş tuvaller kaldırılır, aynı biçimlendirmeye sahip komşu glifler de birleştirilir. Not: Bu özellik olarak ayarlanırsa içerik görüntüsünün doğruluğu etkilenebilir.`doğru` . Varsayılan`doğru` . |
| [PageHorizontalAlignment](../../aspose.words.saving/htmlfixedsaveoptions/pagehorizontalalignment/) { get; set; } | Bir HTML belgesindeki sayfaların yatay hizalamasını belirtir. Varsayılan değerCenter . |
| [PageMargins](../../aspose.words.saving/htmlfixedsaveoptions/pagemargins/) { get; set; } | Bir HTML belgesindeki sayfaların etrafındaki kenar boşluklarını belirtir. Kenar boşluğu değeri puan olarak ölçülür ve 0'a eşit veya büyük olmalıdır. Varsayılan değer 10 puandır. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Bir belge sabit sayfa biçimine aktarıldığında ayrı sayfaların nasıl kaydedileceğini kontrol etmenizi sağlar. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | İşlenecek sayfaları alır veya ayarlar. Varsayılan, belgedeki tüm sayfalardır. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Ne zaman`doğru` , uygun olduğu durumlarda çıktıyı güzel biçimlerde biçimlendirir. Varsayılan değer`YANLIŞ` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Bir belgeyi kaydederken çağrılır ve kaydetme ilerlemesiyle ilgili verileri kabul eder. |
| [RemoveJavaScriptFromLinks](../../aspose.words.saving/htmlfixedsaveoptions/removejavascriptfromlinks/) { get; set; } | JavaScript'in bağlantılardan kaldırılıp kaldırılmayacağını belirtir. Varsayılan`YANLIŞ` . |
| [ResourceSavingCallback](../../aspose.words.saving/htmlfixedsaveoptions/resourcesavingcallback/) { get; set; } | Bir belge sabit sayfalı Html biçimine aktarıldığında kaynakların (resimler, yazı tipleri ve css) nasıl kaydedileceğini kontrol etmenizi sağlar. |
| [ResourcesFolder](../../aspose.words.saving/htmlfixedsaveoptions/resourcesfolder/) { get; set; } | Bir belgeyi Html biçimine aktarırken kaynakların (resimler, yazı tipleri, css) kaydedildiği fiziksel klasörü belirtir. Varsayılan`hükümsüz` . |
| [ResourcesFolderAlias](../../aspose.words.saving/htmlfixedsaveoptions/resourcesfolderalias/) { get; set; } | Bir Html belgesine yazılan görüntü URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan`hükümsüz` . |
| [SaveFontFaceCssSeparately](../../aspose.words.saving/htmlfixedsaveoptions/savefontfacecssseparately/) { get; set; } | Bayrağı, bir belge harici stil sayfasıyla kaydedildiğinde (yani, "@font-face" CSS kurallarının ayrı bir "fontFaces.css" dosyasına yerleştirilip yerleştirilmeyeceğini belirtir.[`ExportEmbeddedCss`](./exportembeddedcss/) şudur`YANLIŞ` ). Varsayılan değer`YANLIŞ` , tüm CSS kuralları tek bir dosyaya yazılır "styles.css". |
| override [SaveFormat](../../aspose.words.saving/htmlfixedsaveoptions/saveformat/) { get; set; } | Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. YalnızcaHtmlFixed . |
| [ShowPageBorder](../../aspose.words.saving/htmlfixedsaveoptions/showpageborder/) { get; set; } | Sayfaların etrafındaki kenarlığın gösterilip gösterilmeyeceğini belirtir. Varsayılan`doğru` . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik`hükümsüz` ve geçici dosyalar kullanılmaz. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Kullanılan karakter koduna göre yazı tipi özniteliklerinin değiştirilip değiştirilmeyeceğini belirler. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Bir değeri alır veya ayarlar.[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) özellik kaydedilmeden önce güncellenir. Varsayılan değer`YANLIŞ` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Belgeyi sabit bir sayfa biçimine kaydetmeden önce belirli türdeki alanların güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. Bu özelliğin varsayılan değeri`doğru` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Bir değeri alır veya ayarlar.[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) özellik kaydedilmeden önce güncellenir. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Bir değeri alır veya ayarlar.[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) özellik kaydedilmeden önce güncellenir. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | İşleme için kenar yumuşatma kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Yüksek kaliteli (yani yavaş) işleme algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar. |
| [UseTargetMachineFonts](../../aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/) { get; set; } | Bayrağı, hedef makinedeki yazı tiplerinin belgeyi görüntülemek için kullanılıp kullanılmayacağını belirtir. Bu bayrak,`doğru` ,[`FontFormat`](./fontformat/) Ve[`ExportEmbeddedFonts`](./exportembeddedfonts/) özelliklerin etkisi yoktur, ayrıca[`ResourceSavingCallback`](./resourcesavingcallback/) fontlar için ateşlenmez. Varsayılan`YANLIŞ` . |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(*object*) | Belirtilen nesnenin geçerli nesneye eşit değerde olup olmadığını belirler. |

## Örnekler

Bir belgeyi HTML'e dönüştürürken oluşturulan harici kaynakların URI'lerini yazdırmak için bir geri aramanın nasıl kullanılacağını gösterir.

```csharp
public void HtmlFixedResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ResourceUriPrinter callback = new ResourceUriPrinter();

    HtmlFixedSaveOptions options = new HtmlFixedSaveOptions
    {
        SaveFormat = SaveFormat.HtmlFixed,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "HtmlFixedResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "HtmlFixedResourceFolderAlias",
        ShowPageBorder = false,
        ResourceSavingCallback = callback
    };

    // ResourcesFolderAlias tarafından belirtilen klasör ResourcesFolder yerine kaynakları içerecektir.
    // Akışların kaynaklarını koyabilmeleri için klasörün var olduğundan emin olmalıyız.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// Sabit HTML'ye dönüştürüldükçe, içerdiği kaynakların URI'lerini sayar ve yazdırır.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        // SaveOptions nesnesinde bir klasör takma adı belirlersek buradan yazdırabileceğiz.
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                // Varsayılan olarak, 'ResourceFileUri' yazı tipleri için sistem klasörünü kullanır.
                // Diğer platformlarda sorun yaşamamak için fontların yolunu açıkça belirtmeniz gerekir.
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // "ResourcesFolderAlias" özelliğinde bir klasör belirttiysek,
        // ayrıca her akışı, kaynağını o klasöre koyacak şekilde yönlendirmemiz gerekecek.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private int mSavedResourceCount;
    private readonly StringBuilder mText = new StringBuilder();
}
```

### Ayrıca bakınız

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
