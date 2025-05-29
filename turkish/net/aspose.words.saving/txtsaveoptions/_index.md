---
title: TxtSaveOptions Class
linktitle: TxtSaveOptions
articleTitle: TxtSaveOptions
second_title: .NET için Aspose.Words
description: Gelişmiş belge kaydetme için Aspose.Words.TxtSaveOptions'ı keşfedin. En iyi sonuçlar için güçlü seçeneklerle metin biçiminizi özelleştirin.
type: docs
weight: 6460
url: /tr/net/aspose.words.saving/txtsaveoptions/
---
## TxtSaveOptions class

Bir belgeyi kaydederken ek seçenekleri belirtmek için kullanılabilirText biçim.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Kaydetme Seçeneklerini Belirleyin](https://docs.aspose.com/words/net/specify-save-options/) belgeleme makalesi.

```csharp
public class TxtSaveOptions : TxtSaveOptionsBase
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [TxtSaveOptions](txtsaveoptions/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AddBidiMarks](../../aspose.words.saving/txtsaveoptions/addbidimarks/) { get; set; } | Düz metin biçiminde dışa aktarırken her BiDi çalışmasından önce çift yönlü işaretlerin eklenip eklenmeyeceğini belirtir. |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | PostScript anahatlarıyla yazı tiplerinin gömülmesine izin verilip verilmeyeceğini belirten bir Boole değeri alır veya ayarlar. Bir belge kaydedildiğinde TrueType yazı tiplerini gömerken. Varsayılan değer`YANLIŞ` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Varsayılan şablona giden yolu alır veya ayarlar (dosya adı dahil). Bu özellik için varsayılan değer**boş dize** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | 3B efektlerin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | DrawingML efektlerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | DrawingML şekillerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [Encoding](../../aspose.words.saving/txtsaveoptionsbase/encoding/) { get; set; } | Metin biçimlerinde dışa aktarırken kullanılacak kodlamayı belirtir. Varsayılan değer**Kodlama.UTF8** . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Ne zaman`doğru` , Aspose.Words adının ve sürümünün üretilen dosyalara gömülmesine neden olur. Varsayılan değer`doğru` . |
| [ExportHeadersFootersMode](../../aspose.words.saving/txtsaveoptionsbase/exportheadersfootersmode/) { get; set; } | Başlıkların ve altbilgilerin metin biçimlerine aktarılma biçimini belirtir. Varsayılan değerPrimaryOnly . |
| [ForcePageBreaks](../../aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/) { get; set; } | Sayfa sonlarının dışa aktarma sırasında korunup korunmayacağını belirtmenizi sağlar. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Mürekkep (InkML) nesnelerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [ListIndentation](../../aspose.words.saving/txtsaveoptions/listindentation/) { get; } | Bir tane alır[`TxtListIndentation`](../txtlistindentation/)liste seviyelerinin girintisi için hangi karakter ve kaç tane kullanılacağını belirten nesne. Varsayılan olarak '\0' karakterinin sayısı sıfırdır, bu girinti olmadığı anlamına gelir. |
| [MaxCharactersPerLine](../../aspose.words.saving/txtsaveoptions/maxcharactersperline/) { get; set; } | Bir satır başına maksimum karakter sayısını belirten bir tamsayı değeri alır veya ayarlar. Varsayılan değer 0'dır, yani sınır yoktur. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Belgeyi kaydetmeden önce bellek optimizasyonunun yapılıp yapılmayacağını belirleyen değeri alır veya ayarlar. Bu özelliğin varsayılan değeri`YANLIŞ` . |
| [ParagraphBreak](../../aspose.words.saving/txtsaveoptionsbase/paragraphbreak/) { get; set; } | Metin biçimlerinde dışa aktarırken paragraf sonu olarak kullanılacak dizeyi belirtir. |
| [PreserveTableLayout](../../aspose.words.saving/txtsaveoptions/preservetablelayout/) { get; set; } | Programın düz metin biçiminde kaydederken tabloların düzenini korumaya çalışıp çalışmayacağını belirtir. Varsayılan değer`YANLIŞ` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Ne zaman`doğru` , uygun olduğu durumlarda çıktıyı güzel biçimlerde biçimlendirir. Varsayılan değer`YANLIŞ` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Bir belgeyi kaydederken çağrılır ve kaydetme ilerlemesiyle ilgili verileri kabul eder. |
| override [SaveFormat](../../aspose.words.saving/txtsaveoptions/saveformat/) { get; set; } | Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. YalnızcaText . |
| [SimplifyListLabels](../../aspose.words.saving/txtsaveoptions/simplifylistlabels/) { get; set; } | Programın, karmaşık etiket biçimlendirmesinin düz metinle yeterince temsil edilmemesi durumunda liste etiketlerini basitleştirip basitleştirmeyeceğini belirtir. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik`hükümsüz` ve geçici dosyalar kullanılmaz. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Kullanılan karakter koduna göre yazı tipi özniteliklerinin değiştirilip değiştirilmeyeceğini belirler. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Bir değeri alır veya ayarlar.[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) özellik kaydedilmeden önce güncellenir. Varsayılan değer`YANLIŞ` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Belgeyi sabit bir sayfa biçimine kaydetmeden önce belirli türdeki alanların güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. Bu özelliğin varsayılan değeri`doğru` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Bir değeri alır veya ayarlar.[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) özellik kaydedilmeden önce güncellenir. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Bir değeri alır veya ayarlar.[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) özellik kaydedilmeden önce güncellenir. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | İşleme için kenar yumuşatma kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Yüksek kaliteli (yani yavaş) işleme algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar. |

## Örnekler

Özel paragraf sonuyla bir .txt belgesinin nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");
builder.Write("Paragraph 3.");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "TxtSaveOptions" nesnesi oluşturun
// Belgeyi düz metne nasıl kaydedeceğimizi değiştirmek için.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

Assert.AreEqual(SaveFormat.Text, txtSaveOptions.SaveFormat);

// "ParagraphBreak" değerini her paragrafın sonuna koymak istediğimiz özel bir değere ayarlayın.
txtSaveOptions.ParagraphBreak = " End of paragraph.\n\n\t";

doc.Save(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt");

Assert.AreEqual("Paragraph 1. End of paragraph.\n\n\t" +
                "Paragraph 2. End of paragraph.\n\n\t" +
                "Paragraph 3. End of paragraph.\n\n\t", docText);
```

### Ayrıca bakınız

* class [TxtSaveOptionsBase](../txtsaveoptionsbase/)
* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
