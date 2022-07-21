---
title: HtmlSaveOptions
second_title: Aspose.Words for .NET API Referansı
description: Bir belgeyi dosyaya kaydederken ek seçenekleri belirtmek için kullanılabilir.Html  Mhtml veyaEpub biçim.
type: docs
weight: 4850
url: /tr/net/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class

Bir belgeyi dosyaya kaydederken ek seçenekleri belirtmek için kullanılabilir.Html , Mhtml veyaEpub biçim.

```csharp
public class HtmlSaveOptions : SaveOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [HtmlSaveOptions](htmlsaveoptions#constructor)() | Bu sınıfın, bir document dosyasını şuraya kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Html biçim. |
| [HtmlSaveOptions](htmlsaveoptions#constructor_1)(SaveFormat) | Bu sınıfın, bir document dosyasını şuraya kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Html ,Mhtml veyaEpub biçim. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | TrueType yazı tiplerini bir belgeye gömerken PostScript anahatlarıyla yazı tiplerinin gömülmesine izin verilip verilmeyeceğini belirten bir boole değeri alır veya ayarlar. Varsayılan değer şudur: **yanlış** . |
| [AllowNegativeIndent](../../aspose.words.saving/htmlsaveoptions/allownegativeindent) { get; set; } | HTML, MHTML veya EPUB'a kaydederken paragrafların negatif sol ve sağ girintilerinin normalize edilip edilmeyeceğini belirtir . Varsayılan değer`yanlış` . |
| [CssClassNamePrefix](../../aspose.words.saving/htmlsaveoptions/cssclassnameprefix) { get; set; } | Tüm CSS sınıfı adlarına eklenen bir önek belirtir. Varsayılan değer boş bir dizedir ve oluşturulan CSS sınıfı adlarının ortak bir öneki yoktur. |
| [CssSavingCallback](../../aspose.words.saving/htmlsaveoptions/csssavingcallback) { get; set; } | Bir belge HTML, MHTML veya EPUB'a kaydedildiğinde CSS stillerinin nasıl kaydedileceğini kontrol etmenizi sağlar. |
| [CssStyleSheetFileName](../../aspose.words.saving/htmlsaveoptions/cssstylesheetfilename) { get; set; } | Bir document HTML'ye aktarıldığında yazılan Basamaklı Stil Sayfası (CSS) dosyasının yolunu ve adını belirtir. Varsayılan boş bir dizedir. |
| [CssStyleSheetType](../../aspose.words.saving/htmlsaveoptions/cssstylesheettype) { get; set; } | CSS (Basamaklı Stil Sayfası) stillerinin HTML, MHTML veya EPUB'a nasıl dışa aktarılacağını belirtir. Varsayılan değerInline HTML/MHTML ve içinExternal EPUB için. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | Varsayılan şablonun yolunu alır veya ayarlar (dosya adı dahil). Bu özellik için varsayılan değer **boş dize** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | 3B efektlerin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | DrawingML efektlerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | DrawingML şekillerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [DocumentPartSavingCallback](../../aspose.words.saving/htmlsaveoptions/documentpartsavingcallback) { get; set; } | Bir belge HTML veya EPUB'a kaydedildiğinde, belge bölümlerinin nasıl kaydedileceğini kontrol etmenizi sağlar. |
| [DocumentSplitCriteria](../../aspose.words.saving/htmlsaveoptions/documentsplitcriteria) { get; set; } | Kaydederken belgenin nasıl bölüneceğini belirtir.Html veyaEpub biçim. VarsayılanNone HTML ve içinHeadingParagraph EPUB için. |
| [DocumentSplitHeadingLevel](../../aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel) { get; set; } | Belgenin bölüneceği maksimum başlık düzeyini belirtir. Varsayılan değer`2` . |
| [Encoding](../../aspose.words.saving/htmlsaveoptions/encoding) { get; set; } | HTML, MHTML veya EPUB'a dışa aktarırken kullanılacak kodlamayı belirtir. Varsayılan değer`yeni UTF8Encoding(yanlış)` (BOM olmadan UTF-8). |
| [EpubNavigationMapLevel](../../aspose.words.saving/htmlsaveoptions/epubnavigationmaplevel) { get; set; } | IDPF EPUB formatına dışa aktarırken navigasyon haritasına doldurulan başlıkların maksimum seviyesini belirtir. Varsayılan değer`3` . |
| [ExportCidUrlsForMhtmlResources](../../aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources) { get; set; } | MHTML belgelerinde bulunan kaynaklara (resimler, yazı tipleri, CSS) başvurmak için CID (İçerik Kimliği) URL'lerinin kullanılıp kullanılmayacağını belirtir. Varsayılan değer`yanlış` . |
| [ExportDocumentProperties](../../aspose.words.saving/htmlsaveoptions/exportdocumentproperties) { get; set; } | Yerleşik ve özel belge özelliklerinin HTML, MHTML veya EPUB'a dışa aktarılıp aktarılmayacağını belirtir. Varsayılan değer`yanlış` . |
| [ExportDropDownFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext) { get; set; } | Açılır form alanlarının HTML veya MHTML'ye nasıl kaydedileceğini kontrol eder. Varsayılan değer`yanlış` . |
| [ExportFontResources](../../aspose.words.saving/htmlsaveoptions/exportfontresources) { get; set; } | Yazı tipi kaynaklarının HTML, MHTML veya EPUB'a aktarılıp aktarılmayacağını belirtir. Varsayılan`yanlış` . |
| [ExportFontsAsBase64](../../aspose.words.saving/htmlsaveoptions/exportfontsasbase64) { get; set; } | Yazı tipi kaynaklarının Base64 kodlamasında HTML'ye gömülmesi gerekip gerekmediğini belirtir. Varsayılan`yanlış` . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | Doğru olduğunda, Aspose.Words'ün adının ve sürümünün üretilen dosyalara gömülmesine neden olur. Varsayılan değerdir **doğru** . |
| [ExportHeadersFootersMode](../../aspose.words.saving/htmlsaveoptions/exportheadersfootersmode) { get; set; } | Üstbilgilerin ve altbilgilerin HTML, MHTML veya EPUB'a nasıl çıkarılacağını belirtir. Varsayılan değerPerSection HTML/MHTML için veNone EPUB için. |
| [ExportImagesAsBase64](../../aspose.words.saving/htmlsaveoptions/exportimagesasbase64) { get; set; } | Görüntülerin HTML, MHTML veya EPUB çıktısına Base64 biçiminde kaydedilip kaydedilmeyeceğini belirtir. Varsayılan`yanlış` . |
| [ExportLanguageInformation](../../aspose.words.saving/htmlsaveoptions/exportlanguageinformation) { get; set; } | Dil bilgilerinin HTML, MHTML veya EPUB'a aktarılıp aktarılmayacağını belirtir. Varsayılan`yanlış` . |
| [ExportListLabels](../../aspose.words.saving/htmlsaveoptions/exportlistlabels) { get; set; } | Liste etiketlerinin HTML, MHTML veya EPUB'a nasıl çıkarılacağını kontrol eder. Varsayılan değerAuto . |
| [ExportOriginalUrlForLinkedImages](../../aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages) { get; set; } | Bağlantılı resimlerin URL'si olarak orijinal URL'nin kullanılıp kullanılmayacağını belirtir. Varsayılan değer`yanlış` . |
| [ExportPageMargins](../../aspose.words.saving/htmlsaveoptions/exportpagemargins) { get; set; } | Sayfa kenar boşluklarının HTML, MHTML veya EPUB olarak dışa aktarılıp aktarılmayacağını belirtir. Varsayılan`yanlış` . |
| [ExportPageSetup](../../aspose.words.saving/htmlsaveoptions/exportpagesetup) { get; set; } | Sayfa düzeninin HTML, MHTML veya EPUB'a aktarılıp aktarılmayacağını belirtir. Varsayılan`yanlış` . |
| [ExportRelativeFontSize](../../aspose.words.saving/htmlsaveoptions/exportrelativefontsize) { get; set; } | HTML, MHTML veya EPUB'a kaydederken yazı tipi boyutlarının ilgili birimlerde çıktısının alınması gerekip gerekmediğini belirtir. Varsayılan`yanlış` . |
| [ExportRoundtripInformation](../../aspose.words.saving/htmlsaveoptions/exportroundtripinformation) { get; set; } | HTML, MHTML veya EPUB'a kaydederken gidiş dönüş bilgilerinin yazıp yazılmayacağını belirtir. Varsayılan değer`doğru` HTML için ve`yanlış` MHTML ve EPUB için. |
| [ExportShapesAsSvg](../../aspose.words.saving/htmlsaveoptions/exportshapesassvg) { get; set; } | [`Shape`](../../aspose.words.drawing/shape) düğümler, HTML, MHTML veya EPUB'a kaydedilirken SVG görüntülerine dönüştürülür. Varsayılan değer`yanlış` . |
| [ExportTextInputFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext) { get; set; } | Metin girişi form alanlarının HTML veya MHTML'ye nasıl kaydedileceğini kontrol eder. Varsayılan değer`yanlış` . |
| [ExportTocPageNumbers](../../aspose.words.saving/htmlsaveoptions/exporttocpagenumbers) { get; set; } | HTML, MHTML ve EPUB kaydedilirken içindekiler tablosuna sayfa numaralarının yazıp yazılmayacağını belirtir. Varsayılan değer`yanlış` . |
| [ExportXhtmlTransitional](../../aspose.words.saving/htmlsaveoptions/exportxhtmltransitional) { get; set; } | HTML'ye mi yoksa MHTML'ye mi kaydedilirken DOCTYPE bildiriminin yazılacağını belirtir. Ne zaman`doğru` , belgeye kök öğeden önce bir DOCTYPE bildirimi yazar. Varsayılan değer`yanlış`. EPUB veya HTML5'e kaydederken (Html5 ) DOCTYPE bildirimi her zaman yazılır. |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | Hangi belge biçimlerinin eşlenmesine izin verildiğini belirleyen değeri alır veya ayarlar.[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . Yalnızca varsayılan olarakFlatOpc belge biçiminin eşlenmesine izin verilir. |
| [FontResourcesSubsettingSizeThreshold](../../aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold) { get; set; } | HTML, MHTML veya EPUB'a kaydederken hangi yazı tipi kaynaklarının alt ayarlanması gerektiğini kontrol eder. Varsayılan`0` . |
| [FontSavingCallback](../../aspose.words.saving/htmlsaveoptions/fontsavingcallback) { get; set; } | Bir belge HTML, MHTML veya EPUB'a kaydedildiğinde yazı tiplerinin nasıl kaydedileceğini kontrol etmenizi sağlar. |
| [FontsFolder](../../aspose.words.saving/htmlsaveoptions/fontsfolder) { get; set; } | Bir belgeyi HTML'ye aktarırken yazı tiplerinin kaydedildiği fiziksel klasörü belirtir. Varsayılan boş bir dizedir. |
| [FontsFolderAlias](../../aspose.words.saving/htmlsaveoptions/fontsfolderalias) { get; set; } | Bir HTML belgesine yazılan yazı tipi URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan boş bir dizedir. |
| [HtmlVersion](../../aspose.words.saving/htmlsaveoptions/htmlversion) { get; set; } | Belgeyi HTML veya MHTML'ye kaydederken kullanılması gereken HTML standardının sürümünü belirtir. Varsayılan değerXhtml . |
| [ImageResolution](../../aspose.words.saving/htmlsaveoptions/imageresolution) { get; set; } | HTML, MHTML veya EPUB'a dışa aktarırken görüntüler için çıktı çözünürlüğünü belirtir. Varsayılan`96 dpi` . |
| [ImageSavingCallback](../../aspose.words.saving/htmlsaveoptions/imagesavingcallback) { get; set; } | Bir belge HTML, MHTML veya EPUB'a kaydedildiğinde resimlerin nasıl kaydedileceğini kontrol etmenizi sağlar. |
| [ImagesFolder](../../aspose.words.saving/htmlsaveoptions/imagesfolder) { get; set; } | Bir belgeyi HTML biçimine aktarırken görüntülerin kaydedildiği fiziksel klasörü belirtir. Varsayılan boş bir dizedir. |
| [ImagesFolderAlias](../../aspose.words.saving/htmlsaveoptions/imagesfolderalias) { get; set; } | Bir HTML belgesine yazılan görüntü URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan boş bir dizedir. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | Mürekkep (InkML) nesnelerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | Belgeyi kaydetmeden önce bellek optimizasyonunun yapılıp yapılmayacağını belirleyen değeri alır veya ayarlar. Bu özellik için varsayılan değer **yanlış** . |
| [MetafileFormat](../../aspose.words.saving/htmlsaveoptions/metafileformat) { get; set; } | HTML, MHTML veya EPUB'a dışa aktarılırken meta dosyalarının hangi biçimde kaydedileceğini belirtir. Varsayılan değerPng , meta dosyalarının PNG görüntülerine raster olarak işlendiği anlamına gelir. |
| [OfficeMathOutputMode](../../aspose.words.saving/htmlsaveoptions/officemathoutputmode) { get; set; } | OfficeMath nesnelerinin HTML, MHTML veya EPUB'a nasıl aktarılacağını denetler. Varsayılan değer`HtmlOfficeMathOutputMode.Image` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | Ne zaman`doğru` , uygun olduğunda güzel biçimler çıktısı. Varsayılan değer **yanlış** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | Bir belge kaydedilirken çağrılır ve ilerleme kaydetmeyle ilgili verileri kabul eder. |
| [ResolveFontNames](../../aspose.words.saving/htmlsaveoptions/resolvefontnames) { get; set; } | Belgede kullanılan yazı tipi ailesi adlarının çözümlenip çözümlenmediğini ve 'ye göre değiştirilip değiştirilmediğini belirtir.[`FontSettings`](../../aspose.words/document/fontsettings) HTML tabanlı biçimlerde yazılırken. |
| [ResourceFolder](../../aspose.words.saving/htmlsaveoptions/resourcefolder) { get; set; } | Bir document HTML'ye dışa aktarıldığında, resimler, yazı tipleri ve harici CSS gibi tüm kaynakların kaydedildiği fiziksel bir klasörü belirtir. Varsayılan boş bir dizedir. |
| [ResourceFolderAlias](../../aspose.words.saving/htmlsaveoptions/resourcefolderalias) { get; set; } | Bir HTML belgesine yazılan tüm kaynakların URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan boş bir dizedir. |
| override [SaveFormat](../../aspose.words.saving/htmlsaveoptions/saveformat) { get; set; } | Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği formatı belirtir. Html ,Mhtml veyaEpub . |
| [ScaleImageToShapeSize](../../aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize) { get; set; } | HTML, MHTML veya EPUB'a dışa aktarılırken görüntülerin Aspose.Words tarafından sınırlayıcı şekil boyutuna ölçeklenip ölçeklenmediğini belirtir. Varsayılan değer`doğru` . |
| [TableWidthOutputMode](../../aspose.words.saving/htmlsaveoptions/tablewidthoutputmode) { get; set; } | Tablo, satır ve hücre genişliklerinin HTML, MHTML veya EPUB'a nasıl aktarılacağını kontrol eder. Varsayılan değerAll . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | Bir DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik`hükümsüz` ve hiçbir geçici dosya kullanılmaz. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | olup olmadığını belirleyen bir değer alır veya ayarlar.[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime) özellik kaydedilmeden önce güncellenir. Varsayılan değer false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | Belgeyi sabit bir sayfa biçimine kaydetmeden önce belirli türlerdeki alanların güncellenmesi gerekip gerekmediğini belirleyen bir değer alır veya ayarlar. Bu özellik için varsayılan değer **doğru** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | olup olmadığını belirleyen bir değer alır veya ayarlar.[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted) özellik kaydedilmeden önce güncellenir. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | olup olmadığını belirleyen bir değer alır veya ayarlar.[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime) özellik kaydedilmeden önce güncellenir. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | İçeriğin olup olmadığını belirleyen değeri alır veya ayarlar.[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag) kaydetmeden önce güncellenir. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | İşleme için kenar yumuşatma kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | Yüksek kaliteli (yani yavaş) işleme algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |

### Örnekler

.html'ye kaydettikten sonra bağlantılı görüntülerin saklanacağı klasörün nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Form alanlarını HTML giriş öğeleri yerine düz metin olarak dışa aktarma seçeneği ayarlayın.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

Bir belgeyi .epub'a kaydederken belirli bir kodlamanın nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Kaydeteceğimiz bir belgenin kodlamasını belirtmek için SaveOptions nesnesini kullanın.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Varsayılan olarak, bir çıktı .epub belgesinin tüm içeriği tek bir HTML bölümünde olacaktır.
// Bölme kriteri, belgeyi birkaç HTML parçasına ayırmamızı sağlar.
// Belgeyi başlık paragraflarına bölmek için kriterleri belirleyeceğiz.
// Bu, belirli bir boyuttan daha önemli HTML dosyalarını okuyamayan okuyucular için kullanışlıdır.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Belge özelliklerini dışa aktarmak istediğimizi belirtin.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

Bir belgenin nasıl parçalara ayrılacağını ve kaydedileceğini gösterir.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "HtmlFixedSaveOptions" nesnesi oluşturun
    // belgeyi HTML'ye nasıl dönüştüreceğimizi değiştirmek için.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Belgeyi normal bir şekilde kaydedersek, bir çıktı HTML olacaktır
    // tüm kaynak belgenin içeriğini içeren belge.
    // "DocumentSplitCriteria" özelliğini "DocumentSplitCriteria.SectionBreak" olarak ayarlayın.
    // belgemizi birden çok HTML dosyasına kaydedin: her bölüm için bir tane.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Belge parçası kaydetme mantığını değiştirmek için "DocumentPartSavingCallback" özelliğine özel bir geri arama atayın.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Görüntü içeren bir belgeyi html'ye dönüştürürsek, birkaç görüntüye bağlanan bir html dosyası elde ederiz.
    // Her görüntü yerel dosya sisteminde bir dosya biçiminde olacaktır.
    // Her görüntünün adını ve dosya sistemi konumunu özelleştirebilen bir geri arama da vardır.
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
        // "Document" özelliği ile kaynak belgenin tamamına erişebiliriz.
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

        // Aspose.Words'ün belgenin her bir bölümünü nereye kaydedeceğini belirlemenin iki yolu aşağıdadır.
        // 1 - Çıktı parça dosyası için bir dosya adı belirleyin:
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
/// Bir HTML dönüşümünün oluşturduğu görüntü dosyaları için özel dosya adları ayarlar.
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

        // Aspose.Words'ün belgenin her bir bölümünü nereye kaydedeceğini belirlemenin iki yolu aşağıdadır.
        // 1 - Çıktı görüntü dosyası için bir dosya adı belirleyin:
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

* class [SaveOptions](../saveoptions)
* ad alanı [Aspose.Words.Saving](../../aspose.words.saving)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
