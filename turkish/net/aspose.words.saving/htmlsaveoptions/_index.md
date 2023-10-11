---
title: Class HtmlSaveOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.HtmlSaveOptions sınıf. Bir belgeyi the ye kaydederken ek seçenekleri belirtmek için kullanılabilirHtml Mhtml Epub  Azw3 veyaMobi format.
type: docs
weight: 5110
url: /tr/net/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class

Bir belgeyi the 'ye kaydederken ek seçenekleri belirtmek için kullanılabilirHtml ,Mhtml ,Epub , Azw3 veyaMobi format.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Kaydetme Seçeneklerini Belirtin](https://docs.aspose.com/words/net/specify-save-options/) dokümantasyon makalesi.

```csharp
public class HtmlSaveOptions : SaveOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [HtmlSaveOptions](htmlsaveoptions/#constructor)() | Bu sınıfın, bir document dosyasını kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Html format. |
| [HtmlSaveOptions](htmlsaveoptions/#constructor_1)(SaveFormat) | Bu sınıfın, bir document dosyasını kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Html ,Mhtml ,Epub , Azw3 veyaMobi format. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Kaydedildikten sonra TrueType yazı tiplerini bir belgeye gömerken PostScript ana hatlarıyla yazı tiplerinin gömülmesine izin verilip verilmeyeceğini belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`YANLIŞ` . |
| [AllowNegativeIndent](../../aspose.words.saving/htmlsaveoptions/allownegativeindent/) { get; set; } | HTML, MHTML veya EPUB'a kaydederken paragrafların negatif sol ve sağ girintilerinin normalize edilip edilmeyeceğini belirtir. Varsayılan değer:`YANLIŞ` . |
| [CssClassNamePrefix](../../aspose.words.saving/htmlsaveoptions/cssclassnameprefix/) { get; set; } | Tüm CSS sınıfı adlarına eklenen bir öneki belirtir. Varsayılan değer boş bir dizedir ve oluşturulan CSS sınıfı adlarının ortak bir öneki yoktur. |
| [CssSavingCallback](../../aspose.words.saving/htmlsaveoptions/csssavingcallback/) { get; set; } | Bir belge HTML, MHTML veya EPUB'a kaydedildiğinde CSS stillerinin nasıl kaydedileceğini kontrol etmenizi sağlar. |
| [CssStyleSheetFileName](../../aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/) { get; set; } | Bir document HTML'ye aktarıldığında yazılan Basamaklı Stil Sayfası (CSS) dosyasının yolunu ve adını belirtir. Varsayılan, boş bir dizedir. |
| [CssStyleSheetType](../../aspose.words.saving/htmlsaveoptions/cssstylesheettype/) { get; set; } | CSS (Basamaklı Stil Sayfası) stillerinin HTML, MHTML veya EPUB'a nasıl aktarılacağını belirtir. Varsayılan değer:Inline HTML/MHTML ve içinExternal EPUB. için |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Varsayılan şablonun yolunu alır veya ayarlar (dosya adı dahil). Bu özellik için varsayılan değer: **boş dize** (Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | 3B efektlerin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | DrawingML efektlerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | DrawingML şekillerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [DocumentPartSavingCallback](../../aspose.words.saving/htmlsaveoptions/documentpartsavingcallback/) { get; set; } | Bir belge HTML veya EPUB'a kaydedildiğinde belge bölümlerinin nasıl kaydedileceğini kontrol etmenizi sağlar. |
| [DocumentSplitCriteria](../../aspose.words.saving/htmlsaveoptions/documentsplitcriteria/) { get; set; } | Belgeyi kaydederken nasıl bölünmesi gerektiğini belirtirHtml , Epub veyaAzw3 biçim. Varsayılan:None HTML ve içinHeadingParagraph EPUB ve AZW3. için |
| [DocumentSplitHeadingLevel](../../aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/) { get; set; } | Belgenin bölüneceği maksimum başlık düzeyini belirtir. Varsayılan değer:`2` . |
| [Encoding](../../aspose.words.saving/htmlsaveoptions/encoding/) { get; set; } | HTML, MHTML veya EPUB'a dışa aktarırken kullanılacak kodlamayı belirtir. Varsayılan değer:`yeni UTF8Kodlama(yanlış)` (BOM olmadan UTF-8). |
| [ExportCidUrlsForMhtmlResources](../../aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources/) { get; set; } | MHTML belgelerinde bulunan kaynaklara (resimler, yazı tipleri, CSS) başvurmak için CID (İçerik Kimliği) URL'lerinin kullanılıp kullanılmayacağını belirtir. Varsayılan değer:`YANLIŞ` . |
| [ExportDocumentProperties](../../aspose.words.saving/htmlsaveoptions/exportdocumentproperties/) { get; set; } | Yerleşik ve özel belge özelliklerinin HTML, MHTML veya EPUB'a aktarılıp aktarılmayacağını belirtir. Varsayılan değer:`YANLIŞ` . |
| [ExportDropDownFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/) { get; set; } | Açılır form alanlarının HTML veya MHTML'ye nasıl kaydedileceğini kontrol eder. Varsayılan değer:`YANLIŞ` . |
| [ExportFontResources](../../aspose.words.saving/htmlsaveoptions/exportfontresources/) { get; set; } | Yazı tipi kaynaklarının HTML'ye mi, MHTML'ye mi yoksa EPUB'a mı aktarılacağını belirtir. Varsayılan:`YANLIŞ` . |
| [ExportFontsAsBase64](../../aspose.words.saving/htmlsaveoptions/exportfontsasbase64/) { get; set; } | Yazı tipi kaynaklarının Base64 kodlamasında HTML'ye gömülmesi gerekip gerekmediğini belirtir. Varsayılan:`YANLIŞ` . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Ne zaman`doğru` , Aspose.Words'ün adının ve sürümünün üretilen dosyalara yerleştirilmesine neden olur. Varsayılan değer:`doğru` . |
| [ExportHeadersFootersMode](../../aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/) { get; set; } | Üstbilgilerin ve altbilgilerin HTML, MHTML veya EPUB'a nasıl aktarılacağını belirtir. Varsayılan değer:PerSection HTML/MHTML için veNone EPUB. için |
| [ExportImagesAsBase64](../../aspose.words.saving/htmlsaveoptions/exportimagesasbase64/) { get; set; } | Görüntülerin HTML, MHTML veya EPUB çıkışına Base64 formatında kaydedilip kaydedilmeyeceğini belirtir. Varsayılan:`YANLIŞ` . |
| [ExportLanguageInformation](../../aspose.words.saving/htmlsaveoptions/exportlanguageinformation/) { get; set; } | Dil bilgilerinin HTML'ye mi, MHTML'ye mi yoksa EPUB'a mı aktarılacağını belirtir. Varsayılan:`YANLIŞ` . |
| [ExportListLabels](../../aspose.words.saving/htmlsaveoptions/exportlistlabels/) { get; set; } | Liste etiketlerinin HTML, MHTML veya EPUB'a nasıl aktarılacağını kontrol eder. Varsayılan değer:Auto . |
| [ExportOriginalUrlForLinkedImages](../../aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/) { get; set; } | Bağlantılı görsellerin URL'si olarak orijinal URL'nin kullanılıp kullanılmayacağını belirtir. Varsayılan değer:`YANLIŞ` . |
| [ExportPageMargins](../../aspose.words.saving/htmlsaveoptions/exportpagemargins/) { get; set; } | Sayfa kenar boşluklarının HTML'ye mi, MHTML'ye mi yoksa EPUB'a mı aktarılacağını belirtir. Varsayılan:`YANLIŞ` . |
| [ExportPageSetup](../../aspose.words.saving/htmlsaveoptions/exportpagesetup/) { get; set; } | Sayfa düzeninin HTML'ye mi, MHTML'ye mi yoksa EPUB'a mı aktarılacağını belirtir. Varsayılan:`YANLIŞ` . |
| [ExportRelativeFontSize](../../aspose.words.saving/htmlsaveoptions/exportrelativefontsize/) { get; set; } | HTML, MHTML veya EPUB'a kaydederken yazı tipi boyutlarının göreli birimler halinde çıkarılıp çıkarılmayacağını belirtir. Varsayılan:`YANLIŞ` . |
| [ExportRoundtripInformation](../../aspose.words.saving/htmlsaveoptions/exportroundtripinformation/) { get; set; } | HTML, MHTML veya EPUB'a kaydederken gidiş-dönüş bilgilerinin yazıp yazmayacağını belirtir. Varsayılan değer:`doğru` HTML için ve`YANLIŞ` MHTML ve EPUB. için |
| [ExportShapesAsSvg](../../aspose.words.saving/htmlsaveoptions/exportshapesassvg/) { get; set; } | olup olmadığını kontrol eder[`Shape`](../../aspose.words.drawing/shape/)düğümler 'yi HTML, MHTML, EPUB veya AZW3'e kaydederken SVG görüntülerine dönüştürülür. Varsayılan değer:`YANLIŞ` . |
| [ExportTextInputFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/) { get; set; } | Metin girişi form alanlarının HTML veya MHTML'ye nasıl kaydedileceğini kontrol eder. Varsayılan değer:`YANLIŞ` . |
| [ExportTocPageNumbers](../../aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/) { get; set; } | HTML, MHTML ve EPUB'u kaydederken içindekiler tablosuna sayfa numaralarının yazıp yazmayacağını belirtir. Varsayılan değer:`YANLIŞ` . |
| [ExportXhtmlTransitional](../../aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/) { get; set; } | HTML'ye veya MHTML'ye kaydederken DOCTYPE bildiriminin yazıp yazmayacağını belirtir. Ne zaman`doğru` , belgede kök öğeden önce bir DOCTYPE bildirimi yazar. Varsayılan değer:`YANLIŞ`. EPUB veya HTML5'e kaydederken (Html5 ) DOCTYPE bildirimi her zaman yazılır. |
| [FontResourcesSubsettingSizeThreshold](../../aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/) { get; set; } | HTML, MHTML veya EPUB'a kaydederken hangi yazı tipi kaynaklarının alt ayarlamaya ihtiyaç duyduğunu kontrol eder. Varsayılan:`0` . |
| [FontSavingCallback](../../aspose.words.saving/htmlsaveoptions/fontsavingcallback/) { get; set; } | Bir belge HTML, MHTML veya EPUB'a kaydedildiğinde yazı tiplerinin nasıl kaydedileceğini kontrol etmenizi sağlar. |
| [FontsFolder](../../aspose.words.saving/htmlsaveoptions/fontsfolder/) { get; set; } | Bir belgeyi HTML'ye aktarırken yazı tiplerinin kaydedildiği fiziksel klasörü belirtir. Varsayılan, boş bir dizedir. |
| [FontsFolderAlias](../../aspose.words.saving/htmlsaveoptions/fontsfolderalias/) { get; set; } | Bir HTML belgesine yazılan yazı tipi URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan, boş bir dizedir. |
| [HtmlVersion](../../aspose.words.saving/htmlsaveoptions/htmlversion/) { get; set; } | Belgeyi HTML veya MHTML'ye kaydederken kullanılması gereken HTML standardı sürümünü belirtir. Varsayılan değer:Xhtml . |
| [ImageResolution](../../aspose.words.saving/htmlsaveoptions/imageresolution/) { get; set; } | HTML, MHTML veya EPUB'a dışa aktarırken görüntülerin çıktı çözünürlüğünü belirtir. Varsayılan:`96 dpi` . |
| [ImageSavingCallback](../../aspose.words.saving/htmlsaveoptions/imagesavingcallback/) { get; set; } | Bir belge HTML, MHTML veya EPUB'a kaydedildiğinde görüntülerin nasıl kaydedileceğini kontrol etmenizi sağlar. |
| [ImagesFolder](../../aspose.words.saving/htmlsaveoptions/imagesfolder/) { get; set; } | Bir belgeyi HTML biçimine dışa aktarırken görüntülerin kaydedildiği fiziksel klasörü belirtir. Varsayılan, boş bir dizedir. |
| [ImagesFolderAlias](../../aspose.words.saving/htmlsaveoptions/imagesfolderalias/) { get; set; } | Bir HTML belgesine yazılan görüntü URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan, boş bir dizedir. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Mürekkep (InkML) nesnelerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Belgeyi kaydetmeden önce bellek optimizasyonunun gerçekleştirilip gerçekleştirilmeyeceğini belirleyen değeri alır veya ayarlar. Bu özellik için varsayılan değer:`YANLIŞ` . |
| [MetafileFormat](../../aspose.words.saving/htmlsaveoptions/metafileformat/) { get; set; } | HTML, MHTML veya EPUB'a dışa aktarırken meta dosyalarının hangi formatta kaydedileceğini belirtir. Varsayılan değer:Png , meta dosyalarının PNG görüntülerine raster olarak işlendiği anlamına gelir. |
| [NavigationMapLevel](../../aspose.words.saving/htmlsaveoptions/navigationmaplevel/) { get; set; } | EPUB, MOBI veya AZW3 formatlarına dışa aktarırken gezinme haritasına doldurulan maksimum başlık düzeyini belirtir. Varsayılan değer:`3` . |
| [OfficeMathOutputMode](../../aspose.words.saving/htmlsaveoptions/officemathoutputmode/) { get; set; } | OfficeMath nesnelerinin HTML, MHTML veya EPUB'a nasıl aktarıldığını kontrol eder. Varsayılan değer:Image . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Ne zaman`doğru` uygulanabilir olduğu yerde güzel formatlarda çıktı. Varsayılan değer:`YANLIŞ` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Bir belge kaydedilirken çağrılır ve kaydetme işlemiyle ilgili verileri kabul eder. |
| [ResolveFontNames](../../aspose.words.saving/htmlsaveoptions/resolvefontnames/) { get; set; } | Belgede kullanılan yazı tipi ailesi adlarının 'ye göre çözümlenip değiştirilmeyeceğini belirtir[`FontSettings`](../../aspose.words/document/fontsettings/) HTML tabanlı formatlara yazılırken. |
| [ResourceFolder](../../aspose.words.saving/htmlsaveoptions/resourcefolder/) { get; set; } | Bir document HTML'ye aktarıldığında görüntüler, yazı tipleri ve harici CSS gibi tüm kaynakların kaydedildiği fiziksel bir klasörü belirtir. Varsayılan boş bir dizedir. |
| [ResourceFolderAlias](../../aspose.words.saving/htmlsaveoptions/resourcefolderalias/) { get; set; } | Bir HTML belgesine yazılan tüm kaynakların URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan, boş bir dizedir. |
| override [SaveFormat](../../aspose.words.saving/htmlsaveoptions/saveformat/) { get; set; } | Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. OlabilirHtml ,Mhtml ,Epub , Azw3 veyaMobi . |
| [ScaleImageToShapeSize](../../aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/) { get; set; } | Görüntülerin HTML, MHTML veya EPUB'a aktarılırken Aspose.Words tarafından sınırlayıcı şekil boyutuna ölçeklenip ölçeklenmeyeceğini belirtir. Varsayılan değer:`doğru` . |
| [TableWidthOutputMode](../../aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/) { get; set; } | Tablo, satır ve hücre genişliklerinin HTML, MHTML veya EPUB'a nasıl aktarıldığını kontrol eder. Varsayılan değer:All . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Bir DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik`hükümsüz` ve hiçbir geçici dosya kullanılmaz. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Bir değer alır veya ayarlar.[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) özellik kaydedilmeden önce güncellenir. Varsayılan değer:`YANLIŞ` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Belgeyi sabit bir sayfa formatında kaydetmeden önce belirli türlerdeki alanların güncellenmesi gerekip gerekmediğini belirleyen bir değer alır veya ayarlar. Bu özellik için varsayılan değer:`doğru` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Bir değer alır veya ayarlar.[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) özellik kaydedilmeden önce güncellenir. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Bir değer alır veya ayarlar.[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) özellik kaydedilmeden önce güncellenir. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Oluşturma için kenar yumuşatma kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Yüksek kaliteli (yani yavaş) oluşturma algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |

### Örnekler

Bağlantılı görsellerin .html'ye kaydedildikten sonra saklanacağı klasörün nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Form alanlarını HTML giriş öğeleri yerine düz metin olarak dışa aktarmak için bir seçenek belirleyin.
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

// Kaydedeceğimiz belgenin kodlamasını belirtmek için SaveOptions nesnesini kullanın.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Varsayılan olarak, bir çıktı .epub belgesinin tüm içeriği tek bir HTML bölümünde bulunur.
// Bölme kriteri, belgeyi birkaç HTML parçasına ayırmamıza olanak tanır.
// Belgeyi başlık paragraflarına bölmek için kriterleri belirleyeceğiz.
// Bu, belirli bir boyuttan daha büyük HTML dosyalarını okuyamayan okuyucular için kullanışlıdır.
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

    // Belgenin "Save" yöntemine aktarabileceğimiz bir "HtmlFixedSaveOptions" nesnesi oluşturun
    // belgeyi HTML'ye nasıl dönüştüreceğimizi değiştirmek için.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Belgeyi normal şekilde kaydedersek tek bir çıktı HTML'si olacaktır
    // kaynak belgenin tüm içeriğini içeren belge.
    // "DocumentSplitCriteria" özelliğini "DocumentSplitCriteria.SectionBreak" olarak ayarlayın
    // belgemizi birden fazla HTML dosyasına kaydedin: her bölüm için bir tane.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Belge bölümü kaydetme mantığını değiştirmek için "DocumentPartSavingCallback" özelliğine özel bir geri çağırma atayın.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Eğer görseller içeren bir belgeyi html'ye dönüştürürsek, birden fazla görsele bağlantı veren bir html dosyası elde ederiz.
    // Her görüntü yerel dosya sisteminde bir dosya biçiminde olacaktır.
    // Her görüntünün adını ve dosya sistemi konumunu özelleştirebilen bir geri çağırma da vardır.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// Kaydetme işleminin bir belgeyi böldüğü çıktı belgeleri için özel dosya adlarını ayarlar.
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
        // Kaynak belgenin tamamına "Belge" özelliği aracılığıyla erişebiliriz.
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

        // Aspose.Words'ün belgenin her bölümünü nereye kaydedeceğini belirlemenin iki yolu aşağıda verilmiştir.
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
/// HTML dönüştürmesinin oluşturduğu görüntü dosyaları için özel dosya adlarını ayarlar.
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

        // Aspose.Words'ün belgenin her bölümünü nereye kaydedeceğini belirlemenin iki yolu aşağıda verilmiştir.
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

* class [SaveOptions](../saveoptions/)
* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


