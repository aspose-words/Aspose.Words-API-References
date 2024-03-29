---
title: TxtSaveOptions Class
linktitle: TxtSaveOptions
articleTitle: TxtSaveOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.TxtSaveOptions sınıf. Bir belgeyi bilgisayara kaydederken ek seçenekleri belirlemek için kullanılabilir.Text format C#'da.
type: docs
weight: 5660
url: /tr/net/aspose.words.saving/txtsaveoptions/
---
## TxtSaveOptions class

Bir belgeyi bilgisayara kaydederken ek seçenekleri belirlemek için kullanılabilir.Text format.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Kaydetme Seçeneklerini Belirtin](https://docs.aspose.com/words/net/specify-save-options/) dokümantasyon makalesi.

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
| [AddBidiMarks](../../aspose.words.saving/txtsaveoptions/addbidimarks/) { get; set; } | Düz metin biçiminde dışa aktarırken her BiDi çalıştırmadan önce çift yönlü işaretlerin eklenip eklenmeyeceğini belirtir. |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Kaydedildikten sonra TrueType yazı tiplerini bir belgeye gömerken PostScript ana hatlarıyla yazı tiplerinin gömülmesine izin verilip verilmeyeceğini belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`YANLIŞ` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Varsayılan şablonun yolunu alır veya ayarlar (dosya adı dahil). Bu özellik için varsayılan değer:**boş dize** (Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | 3B efektlerin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | DrawingML efektlerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | DrawingML şekillerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [Encoding](../../aspose.words.saving/txtsaveoptionsbase/encoding/) { get; set; } | Metin formatlarında dışa aktarırken kullanılacak kodlamayı belirtir. Varsayılan değer:**Kodlama.UTF8** . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Ne zaman`doğru` , Aspose.Words'ün adının ve sürümünün üretilen dosyalara yerleştirilmesine neden olur. Varsayılan değer:`doğru` . |
| [ExportHeadersFootersMode](../../aspose.words.saving/txtsaveoptionsbase/exportheadersfootersmode/) { get; set; } | Üstbilgilerin ve altbilgilerin metin formatlarına aktarılma yöntemini belirtir. Varsayılan değer:PrimaryOnly . |
| [ForcePageBreaks](../../aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/) { get; set; } | Dışa aktarma sırasında sayfa sonlarının korunup korunmayacağını belirtmenize olanak tanır. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Mürekkep (InkML) nesnelerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [ListIndentation](../../aspose.words.saving/txtsaveoptions/listindentation/) { get; } | Bir alır[`TxtListIndentation`](../txtlistindentation/) liste seviyelerinin girintisi için kaç karakterin ve hangi karakterin kullanılacağını belirten nesne. Varsayılan olarak '\0' karakterinin sayısı sıfırdır, bu da girinti olmadığı anlamına gelir. |
| [MaxCharactersPerLine](../../aspose.words.saving/txtsaveoptions/maxcharactersperline/) { get; set; } | Bir satır başına maksimum karakter sayısını belirten bir tamsayı değeri alır veya ayarlar. Varsayılan değer 0'dır, yani sınır yoktur. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Belgeyi kaydetmeden önce bellek optimizasyonunun gerçekleştirilip gerçekleştirilmeyeceğini belirleyen değeri alır veya ayarlar. Bu özellik için varsayılan değer:`YANLIŞ` . |
| [ParagraphBreak](../../aspose.words.saving/txtsaveoptionsbase/paragraphbreak/) { get; set; } | Metin formatlarında dışa aktarırken paragraf sonu olarak kullanılacak dizeyi belirtir. |
| [PreserveTableLayout](../../aspose.words.saving/txtsaveoptions/preservetablelayout/) { get; set; } | Programın, düz metin biçiminde kaydederken tabloların düzenini korumaya çalışıp çalışmayacağını belirtir. Varsayılan değer:`YANLIŞ` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Ne zaman`doğru` uygulanabilir olduğu yerde güzel formatlarda çıktı. Varsayılan değer:`YANLIŞ` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Bir belge kaydedilirken çağrılır ve kaydetme işlemiyle ilgili verileri kabul eder. |
| override [SaveFormat](../../aspose.words.saving/txtsaveoptions/saveformat/) { get; set; } | Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. YalnızcaText . |
| [SimplifyListLabels](../../aspose.words.saving/txtsaveoptions/simplifylistlabels/) { get; set; } | karmaşık etiket biçimlendirmesinin düz metinle yeterince temsil edilmemesi durumunda programın liste etiketlerini basitleştirip basitleştirmeyeceğini belirtir. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Bir DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik`hükümsüz` ve hiçbir geçici dosya kullanılmaz. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Bir değer alır veya ayarlar.[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) özellik kaydedilmeden önce güncellenir. Varsayılan değer:`YANLIŞ` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Belgeyi sabit bir sayfa formatında kaydetmeden önce belirli türlerdeki alanların güncellenmesi gerekip gerekmediğini belirleyen bir değer alır veya ayarlar. Bu özellik için varsayılan değer:`doğru` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Bir değer alır veya ayarlar.[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) özellik kaydedilmeden önce güncellenir. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Bir değer alır veya ayarlar.[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) özellik kaydedilmeden önce güncellenir. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Oluşturma için kenar yumuşatma kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Yüksek kaliteli (yani yavaş) oluşturma algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |

## Örnekler

Bir .txt belgesinin özel paragraf sonuyla nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");
builder.Write("Paragraph 3.");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "TxtSaveOptions" nesnesi oluşturun
// belgeyi düz metne kaydetme şeklimizi değiştirmek için.
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
