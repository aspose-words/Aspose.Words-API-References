---
title: HtmlSaveOptions Class
linktitle: HtmlSaveOptions
articleTitle: HtmlSaveOptions
second_title: .NET için Aspose.Words
description: HTML, MHTML, EPUB, AZW3 ve MOBI formatlarındaki belge kaydetmeyi özelleştirilebilir seçeneklerle geliştirmek için Aspose.Words.Saving.HtmlSaveOptions'ı keşfedin.
type: docs
weight: 5860
url: /tr/net/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class

Bir belgeyi klasörüne kaydederken ek seçenekleri belirtmek için kullanılabilir.Html ,Mhtml ,Epub , Azw3 veyaMobi biçim.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Kaydetme Seçeneklerini Belirleyin](https://docs.aspose.com/words/net/specify-save-options/) belgeleme makalesi.

```csharp
public class HtmlSaveOptions : SaveOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [HtmlSaveOptions](htmlsaveoptions/#constructor)() | Bu sınıfın, bir document dosyasını kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Html biçim. |
| [HtmlSaveOptions](htmlsaveoptions/#constructor_1)(*[SaveFormat](../../aspose.words/saveformat/)*) | Bu sınıfın, bir document dosyasını kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Html ,Mhtml ,Epub , Azw3 veyaMobi biçim. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | PostScript anahatlarıyla yazı tiplerinin gömülmesine izin verilip verilmeyeceğini belirten bir Boole değeri alır veya ayarlar. Bir belge kaydedildiğinde TrueType yazı tiplerini gömerken. Varsayılan değer`YANLIŞ` . |
| [AllowNegativeIndent](../../aspose.words.saving/htmlsaveoptions/allownegativeindent/) { get; set; } | HTML, MHTML veya EPUB'a kaydederken paragrafların negatif sol ve sağ girintilerinin normalleştirilip normalleştirilmeyeceğini belirtir. Varsayılan değer`YANLIŞ` . |
| [CssClassNamePrefix](../../aspose.words.saving/htmlsaveoptions/cssclassnameprefix/) { get; set; } | Tüm CSS sınıf adlarına eklenen bir önek belirtir. Varsayılan değer boş bir dizedir ve oluşturulan CSS sınıf adlarının ortak bir öneki yoktur. |
| [CssSavingCallback](../../aspose.words.saving/htmlsaveoptions/csssavingcallback/) { get; set; } | Bir belge HTML, MHTML veya EPUB olarak kaydedildiğinde CSS stillerinin nasıl kaydedileceğini kontrol etmenizi sağlar. |
| [CssStyleSheetFileName](../../aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/) { get; set; } | Bir belge HTML'e aktarıldığında yazılan Basamaklı Stil Sayfası (CSS) dosyasının yolunu ve adını belirtir. Varsayılan boş bir dizedir. |
| [CssStyleSheetType](../../aspose.words.saving/htmlsaveoptions/cssstylesheettype/) { get; set; } | CSS (Basamaklı Stil Sayfası) stillerinin HTML, MHTML veya EPUB'a nasıl aktarılacağını belirtir. Varsayılan değerInline HTML/MHTML ve içinExternal EPUB için. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Varsayılan şablona giden yolu alır veya ayarlar (dosya adı dahil). Bu özellik için varsayılan değer**boş dize** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | 3B efektlerin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | DrawingML efektlerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | DrawingML şekillerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [DocumentPartSavingCallback](../../aspose.words.saving/htmlsaveoptions/documentpartsavingcallback/) { get; set; } | Bir belge HTML veya EPUB olarak kaydedildiğinde belge bölümlerinin nasıl kaydedileceğini kontrol etmenizi sağlar. |
| [DocumentSplitCriteria](../../aspose.words.saving/htmlsaveoptions/documentsplitcriteria/) { get; set; } | Belgenin kaydedilirken nasıl bölüneceğini belirtirHtml , Epub veyaAzw3 format. VarsayılanNone HTML ve içinHeadingParagraph EPUB ve AZW3 için. |
| [DocumentSplitHeadingLevel](../../aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/) { get; set; } | Belgenin bölüneceği başlıkların maksimum düzeyini belirtir. Varsayılan değer`2` . |
| [Encoding](../../aspose.words.saving/htmlsaveoptions/encoding/) { get; set; } | HTML, MHTML veya EPUB'a aktarırken kullanılacak kodlamayı belirtir. Varsayılan değer`yeni UTF8Kodlama(yanlış)` (BOM olmadan UTF-8). |
| [ExportCidUrlsForMhtmlResources](../../aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources/) { get; set; } | MHTML belgelerinde yer alan kaynaklara (görüntüler, yazı tipleri, CSS) başvurmak için CID (İçerik Kimliği) URL'lerinin kullanılıp kullanılmayacağını belirtir. Varsayılan değer`YANLIŞ` . |
| [ExportDocumentProperties](../../aspose.words.saving/htmlsaveoptions/exportdocumentproperties/) { get; set; } | Yerleşik ve özel belge özelliklerinin HTML, MHTML veya EPUB'a aktarılıp aktarılmayacağını belirtir. Varsayılan değer`YANLIŞ` . |
| [ExportDropDownFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/) { get; set; } | Açılır form alanlarının HTML veya MHTML'ye nasıl kaydedileceğini kontrol eder. Varsayılan değer`YANLIŞ` . |
| [ExportFontResources](../../aspose.words.saving/htmlsaveoptions/exportfontresources/) { get; set; } | Yazı tipi kaynaklarının HTML, MHTML veya EPUB'a aktarılıp aktarılmayacağını belirtir. Varsayılan`YANLIŞ` . |
| [ExportFontsAsBase64](../../aspose.words.saving/htmlsaveoptions/exportfontsasbase64/) { get; set; } | Yazı tipi kaynaklarının HTML'ye Base64 kodlamasıyla gömülmesi gerekip gerekmediğini belirtir. Varsayılan`YANLIŞ` . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Ne zaman`doğru` , Aspose.Words adının ve sürümünün üretilen dosyalara gömülmesine neden olur. Varsayılan değer`doğru` . |
| [ExportHeadersFootersMode](../../aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/) { get; set; } | Başlıkların ve altbilgilerin HTML, MHTML veya EPUB'a nasıl çıktılanacağını belirtir. Varsayılan değerPerSection HTML/MHTML ve içinNone EPUB için. |
| [ExportImagesAsBase64](../../aspose.words.saving/htmlsaveoptions/exportimagesasbase64/) { get; set; } | Görüntülerin çıktı HTML, MHTML veya EPUB'a Base64 biçiminde kaydedilip kaydedilmeyeceğini belirtir. Varsayılan`YANLIŞ` . |
| [ExportLanguageInformation](../../aspose.words.saving/htmlsaveoptions/exportlanguageinformation/) { get; set; } | Dil bilgilerinin HTML, MHTML veya EPUB'a aktarılıp aktarılmayacağını belirtir. Varsayılan`YANLIŞ` . |
| [ExportListLabels](../../aspose.words.saving/htmlsaveoptions/exportlistlabels/) { get; set; } | Liste etiketlerinin HTML, MHTML veya EPUB'a nasıl çıktılanacağını kontrol eder. Varsayılan değerAuto . |
| [ExportOriginalUrlForLinkedImages](../../aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/) { get; set; } | Bağlantılı resimlerin URL'si olarak orijinal URL'nin kullanılıp kullanılmayacağını belirtir. Varsayılan değer`YANLIŞ` . |
| [ExportPageMargins](../../aspose.words.saving/htmlsaveoptions/exportpagemargins/) { get; set; } | Sayfa kenar boşluklarının HTML, MHTML veya EPUB olarak dışa aktarılıp aktarılmayacağını belirtir. Varsayılan`YANLIŞ` . |
| [ExportPageSetup](../../aspose.words.saving/htmlsaveoptions/exportpagesetup/) { get; set; } | Sayfa düzeninin HTML, MHTML veya EPUB'a aktarılıp aktarılmayacağını belirtir. Varsayılan`YANLIŞ` . |
| [ExportRelativeFontSize](../../aspose.words.saving/htmlsaveoptions/exportrelativefontsize/) { get; set; } | HTML, MHTML veya EPUB'a kaydederken yazı tipi boyutlarının göreli birimlerde çıktı verilip verilmeyeceğini belirtir. Varsayılan`YANLIŞ` . |
| [ExportRoundtripInformation](../../aspose.words.saving/htmlsaveoptions/exportroundtripinformation/) { get; set; } | HTML, MHTML veya EPUB'a kaydederken gidiş-dönüş bilgilerinin yazılıp yazılmayacağını belirtir. Varsayılan değer`doğru` HTML ve için`YANLIŞ` MHTML ve EPUB için. |
| [ExportShapesAsSvg](../../aspose.words.saving/htmlsaveoptions/exportshapesassvg/) { get; set; } | Kontroller[`Shape`](../../aspose.words.drawing/shape/)düğümler, saving HTML, MHTML, EPUB veya AZW3'e dönüştürüldüğünde SVG görüntülerine dönüştürülür. Varsayılan değer`YANLIŞ` . |
| [ExportTextInputFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/) { get; set; } | Metin girişi form alanlarının HTML veya MHTML'ye nasıl kaydedileceğini kontrol eder. Varsayılan değer`YANLIŞ` . |
| [ExportTocPageNumbers](../../aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/) { get; set; } | HTML, MHTML ve EPUB kaydedilirken içerik tablosuna sayfa numaralarının yazılıp yazılmayacağını belirtir. Varsayılan değer`YANLIŞ` . |
| [ExportXhtmlTransitional](../../aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/) { get; set; } | HTML veya MHTML'ye kaydederken DOCTYPE bildiriminin yazılıp yazılamayacağını belirtir. `doğru` , kök öğeden önce belgeye bir DOCTYPE bildirimi yazar. Varsayılan değer`YANLIŞ`. EPUB veya HTML5'e kaydederken (Html5 ) DOCTYPE bildirimi her zaman yazılır. |
| [FontResourcesSubsettingSizeThreshold](../../aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/) { get; set; } | HTML, MHTML veya EPUB'a kaydederken hangi yazı tipi kaynaklarının alt kümeye ayrılması gerektiğini kontrol eder. Varsayılan`0` . |
| [FontSavingCallback](../../aspose.words.saving/htmlsaveoptions/fontsavingcallback/) { get; set; } | Bir belge HTML, MHTML veya EPUB olarak kaydedildiğinde yazı tiplerinin nasıl kaydedileceğini kontrol etmenizi sağlar. |
| [FontsFolder](../../aspose.words.saving/htmlsaveoptions/fontsfolder/) { get; set; } | Bir belgeyi HTML'ye aktarırken yazı tiplerinin kaydedildiği fiziksel klasörü belirtir. Varsayılan boş bir dizedir. |
| [FontsFolderAlias](../../aspose.words.saving/htmlsaveoptions/fontsfolderalias/) { get; set; } | Bir HTML belgesine yazılan yazı tipi URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan boş bir dizedir. |
| [HtmlVersion](../../aspose.words.saving/htmlsaveoptions/htmlversion/) { get; set; } | Belgeyi HTML veya MHTML olarak kaydederken kullanılması gereken HTML standardının sürümünü belirtir. Varsayılan değerXhtml . |
| [ImageResolution](../../aspose.words.saving/htmlsaveoptions/imageresolution/) { get; set; } | HTML, MHTML veya EPUB'a aktarırken görüntülerin çıktı çözünürlüğünü belirtir. Varsayılan`96 dpi` . |
| [ImageSavingCallback](../../aspose.words.saving/htmlsaveoptions/imagesavingcallback/) { get; set; } | Bir belge HTML, MHTML veya EPUB olarak kaydedildiğinde görüntülerin nasıl kaydedileceğini kontrol etmenizi sağlar. |
| [ImagesFolder](../../aspose.words.saving/htmlsaveoptions/imagesfolder/) { get; set; } | Bir belgeyi HTML biçimine aktarırken görüntülerin kaydedileceği fiziksel klasörü belirtir. Varsayılan boş bir dizedir. |
| [ImagesFolderAlias](../../aspose.words.saving/htmlsaveoptions/imagesfolderalias/) { get; set; } | Bir HTML belgesine yazılan görüntü URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan boş bir dizedir. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Mürekkep (InkML) nesnelerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Belgeyi kaydetmeden önce bellek optimizasyonunun yapılıp yapılmayacağını belirleyen değeri alır veya ayarlar. Bu özelliğin varsayılan değeri`YANLIŞ` . |
| [MetafileFormat](../../aspose.words.saving/htmlsaveoptions/metafileformat/) { get; set; } | HTML, MHTML veya EPUB'a aktarırken meta dosyalarının hangi biçimde kaydedileceğini belirtir. Varsayılan değerPng , meta dosyalarının raster PNG görüntülerine dönüştürüldüğü anlamına gelir. |
| [NavigationMapLevel](../../aspose.words.saving/htmlsaveoptions/navigationmaplevel/) { get; set; } | EPUB, MOBI veya AZW3 biçimlerine aktarırken gezinme haritasına doldurulacak başlıkların maksimum düzeyini belirtir. Varsayılan değer`3` . |
| [OfficeMathOutputMode](../../aspose.words.saving/htmlsaveoptions/officemathoutputmode/) { get; set; } | OfficeMath nesnelerinin HTML, MHTML veya EPUB'a nasıl aktarılacağını denetler. Varsayılan değerImage . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Ne zaman`doğru` , uygun olduğu durumlarda çıktıyı güzel biçimlerde biçimlendirir. Varsayılan değer`YANLIŞ` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Bir belgeyi kaydederken çağrılır ve kaydetme ilerlemesiyle ilgili verileri kabul eder. |
| [RemoveJavaScriptFromLinks](../../aspose.words.saving/htmlsaveoptions/removejavascriptfromlinks/) { get; set; } | JavaScript'in bağlantılardan kaldırılıp kaldırılmayacağını belirtir. Varsayılan`YANLIŞ` . |
| [ReplaceBackslashWithYenSign](../../aspose.words.saving/htmlsaveoptions/replacebackslashwithyensign/) { get; set; } | Ters eğik çizgi karakterlerinin yen işaretleriyle değiştirilip değiştirilmeyeceğini belirtir. Varsayılan değer`YANLIŞ` . |
| [ResolveFontNames](../../aspose.words.saving/htmlsaveoptions/resolvefontnames/) { get; set; } | Belgede kullanılan yazı tipi aile adlarının çözümlenip çözümlenmeyeceğini ve 'ye göre değiştirilip değiştirilmeyeceğini belirtir[`FontSettings`](../../aspose.words/document/fontsettings/) HTML tabanlı formatlara yazıldığında. |
| [ResourceFolder](../../aspose.words.saving/htmlsaveoptions/resourcefolder/) { get; set; } | Bir belge HTML'ye aktarıldığında, resimler, yazı tipleri ve harici CSS gibi tüm kaynakların kaydedildiği fiziksel bir klasörü belirtir. Varsayılan boş bir dizedir. |
| [ResourceFolderAlias](../../aspose.words.saving/htmlsaveoptions/resourcefolderalias/) { get; set; } | Bir HTML belgesine yazılan tüm kaynakların URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan boş bir dizedir. |
| override [SaveFormat](../../aspose.words.saving/htmlsaveoptions/saveformat/) { get; set; } | Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. Html ,Mhtml ,Epub , Azw3 veyaMobi . |
| [ScaleImageToShapeSize](../../aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/) { get; set; } | HTML, MHTML veya EPUB'a aktarırken görüntülerin Aspose.Words tarafından sınırlayıcı şekil boyutuna ölçeklenip ölçeklenmeyeceğini belirtir. Varsayılan değer`doğru` . |
| [TableWidthOutputMode](../../aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/) { get; set; } | Tablo, satır ve hücre genişliklerinin HTML, MHTML veya EPUB'a nasıl aktarılacağını kontrol eder. Varsayılan değerAll . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik`hükümsüz` ve geçici dosyalar kullanılmaz. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Kullanılan karakter koduna göre yazı tipi özniteliklerinin değiştirilip değiştirilmeyeceğini belirler. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Bir değeri alır veya ayarlar.[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) özellik kaydedilmeden önce güncellenir. Varsayılan değer`YANLIŞ` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Belgeyi sabit bir sayfa biçimine kaydetmeden önce belirli türdeki alanların güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. Bu özelliğin varsayılan değeri`doğru` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Bir değeri alır veya ayarlar.[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) özellik kaydedilmeden önce güncellenir. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Bir değeri alır veya ayarlar.[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) özellik kaydedilmeden önce güncellenir. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | İşleme için kenar yumuşatma kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Yüksek kaliteli (yani yavaş) işleme algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar. |

## Örnekler

Bağlantılı görsellerin .html olarak kaydedildikten sonra saklanacağı klasörün nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Form alanlarını HTML giriş öğeleri yerine düz metin olarak dışa aktarmak için bir seçenek ayarlayın.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

Bir belgeyi .epub olarak kaydederken belirli bir kodlamanın nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Kaydedeceğimiz belgenin kodlamasını belirtmek için SaveOptions nesnesini kullanın.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Varsayılan olarak, bir çıktı .epub belgesinin tüm içeriği tek bir HTML parçasında olacaktır.
// Bölme kriteri, belgeyi birkaç HTML parçasına ayırmamızı sağlar.
// Belgeyi başlık paragraflarına bölme kriterini belirleyeceğiz.
// Bu, belirli bir boyuttan daha büyük HTML dosyalarını okuyamayan okuyucular için yararlıdır.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Belge özelliklerini dışa aktarmak istediğimizi belirtelim.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

Bir belgenin parçalara nasıl bölüneceğini ve kaydedileceğini gösterir.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Belgenin "Kaydet" metoduna geçirebileceğimiz bir "HtmlFixedSaveOptions" nesnesi oluşturun
    // Belgeyi HTML'ye nasıl dönüştüreceğimizi değiştirmek için.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Belgeyi normal şekilde kaydedersek, bir HTML çıktısı olacaktır
    // kaynak belgenin tüm içeriğini içeren belge.
    // "DocumentSplitCriteria" özelliğini "DocumentSplitCriteria.SectionBreak" olarak ayarlayın
    // Belgemizi birden fazla HTML dosyasına kaydedelim: her bölüm için bir tane.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Belge parçası kaydetme mantığını değiştirmek için "DocumentPartSavingCallback" özelliğine özel bir geri arama atayın.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Resim içeren bir belgeyi html'e dönüştürürsek, birden fazla resme bağlantı veren tek bir html dosyası elde ederiz.
    // Her görüntü yerel dosya sisteminde bir dosya biçiminde olacak.
    // Ayrıca her bir görüntünün adını ve dosya sistemi konumunu özelleştirebilen bir geri çağırma da vardır.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// Kaydetme işleminin bir belgeyi böldüğü çıktı belgeleri için özel dosya adları ayarlar.
/// </summary>
private class SavedDocumentPartRename : IDocumentPartSavingCallback
{
    public SavedDocumentPartRename(string outFileName, DocumentSplitCriteria documentSplitCriteria)
    {
        mOutFileName = outFileName;
        mDocumentSplitCriteria = documentSplitCriteria;
    }

    void IDocumentPartSavingCallback.DocumentPartSaving(DocumentPartSavingArgs args)
    {
        // "Belge" özelliği aracılığıyla kaynak belgenin tamamına erişebiliriz.
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        string partType = string.Empty;

        switch (mDocumentSplitCriteria)
        {
            case DocumentSplitCriteria.PageBreak:
                partType = "Page";
                break;
            case DocumentSplitCriteria.ColumnBreak:
                partType = "Column";
                break;
            case DocumentSplitCriteria.SectionBreak:
                partType = "Section";
                break;
            case DocumentSplitCriteria.HeadingParagraph:
                partType = "Paragraph from heading";
                break;
        }

        string partFileName = $"{mOutFileName} part {++mCount}, of type {partType}{Path.GetExtension(args.DocumentPartFileName)}";

        // Aşağıda Aspose.Words'ün belgenin her bir bölümünü nereye kaydedeceğini belirtmenin iki yolu bulunmaktadır.
        // 1 - Çıktı parçası dosyası için bir dosya adı belirleyin:
        args.DocumentPartFileName = partFileName;

        // 2 - Çıktı parça dosyası için özel bir akış oluşturun:
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// HTML dönüşümünün oluşturduğu resim dosyaları için özel dosya adları ayarlar.
/// </summary>
public class SavedImageRename : IImageSavingCallback
{
    public SavedImageRename(string outFileName)
    {
        mOutFileName = outFileName;
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        string imageFileName = $"{mOutFileName} shape {++mCount}, of type {args.CurrentShape.ShapeType}{Path.GetExtension(args.ImageFileName)}";

        // Aşağıda Aspose.Words'ün belgenin her bir bölümünü nereye kaydedeceğini belirtmenin iki yolu bulunmaktadır.
        // 1 - Çıkış görüntü dosyası için bir dosya adı belirleyin:
        args.ImageFileName = imageFileName;

        // 2 - Çıktı görüntü dosyası için özel bir akış oluşturun:
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.True(args.ImageStream.CanWrite);
        Assert.True(args.IsImageAvailable);
        Assert.False(args.KeepImageStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

### Ayrıca bakınız

* class [SaveOptions](../saveoptions/)
* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
