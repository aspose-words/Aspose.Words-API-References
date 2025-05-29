---
title: CompareOptions Class
linktitle: CompareOptions
articleTitle: CompareOptions
second_title: .NET için Aspose.Words
description: Gelişmiş belge karşılaştırması için Aspose.Words.CompareOptions sınıfını keşfedin. Hassas sonuçlar ve gelişmiş üretkenlik için karşılaştırma ayarlarınızı özelleştirin.
type: docs
weight: 470
url: /tr/net/aspose.words.comparing/compareoptions/
---
## CompareOptions class

Belge karşılaştırma işlemi için ek seçeneklerin seçilmesine olanak tanır.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Belgeleri Karşılaştır](https://docs.aspose.com/words/net/compare-documents/) belgeleme makalesi.

```csharp
public class CompareOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [CompareOptions](compareoptions/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AdvancedOptions](../../aspose.words.comparing/compareoptions/advancedoptions/) { get; } | Daha kesin karşılaştırma çıktısı üretmeye yardımcı olabilecek gelişmiş karşılaştırma seçeneklerini belirtir. |
| [CompareMoves](../../aspose.words.comparing/compareoptions/comparemoves/) { get; set; } | İki belge arasındaki farkların karşılaştırılıp karşılaştırılmayacağını belirtir. |
| [Granularity](../../aspose.words.comparing/compareoptions/granularity/) { get; set; } | Değişikliklerin karakter bazında mı yoksa kelime bazında mı izlendiğini belirtir. |
| [IgnoreCaseChanges](../../aspose.words.comparing/compareoptions/ignorecasechanges/) { get; set; } | True, belge karşılaştırmasının büyük/küçük harfe duyarlı olmadığını gösterir. |
| [IgnoreComments](../../aspose.words.comparing/compareoptions/ignorecomments/) { get; set; } | Yorumlardaki farklılıkların karşılaştırılıp karşılaştırılmayacağını belirtir. |
| [IgnoreFields](../../aspose.words.comparing/compareoptions/ignorefields/) { get; set; } | Alanlardaki farklılıkların karşılaştırılıp karşılaştırılmayacağını belirtir. |
| [IgnoreFootnotes](../../aspose.words.comparing/compareoptions/ignorefootnotes/) { get; set; } | Dipnotlar ve sonnotlardaki farklılıkların karşılaştırılıp karşılaştırılmayacağını belirtir. |
| [IgnoreFormatting](../../aspose.words.comparing/compareoptions/ignoreformatting/) { get; set; } | True, biçimlendirmenin göz ardı edildiğini gösterir. |
| [IgnoreHeadersAndFooters](../../aspose.words.comparing/compareoptions/ignoreheadersandfooters/) { get; set; } | True, başlık ve altbilgi içeriğinin göz ardı edildiğini gösterir. |
| [IgnoreTables](../../aspose.words.comparing/compareoptions/ignoretables/) { get; set; } | Tablolarda bulunan verilerdeki farklılıkların karşılaştırılıp karşılaştırılmayacağını belirtir. |
| [IgnoreTextboxes](../../aspose.words.comparing/compareoptions/ignoretextboxes/) { get; set; } | Metin kutularında bulunan verilerdeki farklılıkların karşılaştırılıp karşılaştırılmayacağını belirtir. |
| [Target](../../aspose.words.comparing/compareoptions/target/) { get; set; } | Karşılaştırma sırasında hedef olarak hangi belgenin kullanılacağını belirtir. |

## Örnekler

Karşılaştırma yaparken belirli türdeki belge öğelerinin nasıl filtreleneceğini gösterir.

```csharp
// Orijinal belgeyi oluştur ve çeşitli öğelerle doldur.
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);

// Dipnotla referans verilen paragraf metni:
builder.Writeln("Hello world! This is the first paragraph.");
builder.InsertFootnote(FootnoteType.Endnote, "Original endnote text.");

// Masa:
builder.StartTable();
builder.InsertCell();
builder.Write("Original cell 1 text");
builder.InsertCell();
builder.Write("Original cell 2 text");
builder.EndTable();

// Metin kutusu:
Shape textBox = builder.InsertShape(ShapeType.TextBox, 150, 20);
builder.MoveTo(textBox.FirstParagraph);
builder.Write("Original textbox contents");

// TARİH alanı:
builder.MoveTo(docOriginal.FirstSection.Body.AppendParagraph(""));
builder.InsertField(" DATE ");

// Yorum:
Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", DateTime.Now);
newComment.SetText("Original comment.");
builder.CurrentParagraph.AppendChild(newComment);

// Başlık:
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Original header contents.");

// Belgemizin bir klonunu oluşturalım ve klonlanan belgenin her bir öğesinde hızlı bir düzenleme yapalım.
Document docEdited = (Document)docOriginal.Clone(true);
Paragraph firstParagraph = docEdited.FirstSection.Body.FirstParagraph;

firstParagraph.Runs[0].Text = "hello world! this is the first paragraph, after editing.";
firstParagraph.ParagraphFormat.Style = docEdited.Styles[StyleIdentifier.Heading1];
((Footnote)docEdited.GetChild(NodeType.Footnote, 0, true)).FirstParagraph.Runs[1].Text = "Edited endnote text.";
((Table)docEdited.GetChild(NodeType.Table, 0, true)).FirstRow.Cells[1].FirstParagraph.Runs[0].Text = "Edited Cell 2 contents";
((Shape)docEdited.GetChild(NodeType.Shape, 0, true)).FirstParagraph.Runs[0].Text = "Edited textbox contents";
((FieldDate)docEdited.Range.Fields[0]).UseLunarCalendar = true;
((Comment)docEdited.GetChild(NodeType.Comment, 0, true)).FirstParagraph.Runs[0].Text = "Edited comment.";
docEdited.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].FirstParagraph.Runs[0].Text =
    "Edited header contents.";

// Belgeleri karşılaştırmak, düzenlenen belgedeki her düzenleme için bir revizyon oluşturur.
// Bir CompareOptions nesnesi, revizyonları bastırabilen bir dizi bayrak içerir
// her bir öğenin kendi türünde, değişikliklerini etkili bir şekilde görmezden gelerek.
CompareOptions compareOptions = new CompareOptions
{
    CompareMoves = false,
    IgnoreFormatting = false,
    IgnoreCaseChanges = false,
    IgnoreComments = false,
    IgnoreTables = false,
    IgnoreFields = false,
    IgnoreFootnotes = false,
    IgnoreTextboxes = false,
    IgnoreHeadersAndFooters = false,
    Target = ComparisonTargetType.New
};

docOriginal.Compare(docEdited, "John Doe", DateTime.Now, compareOptions);
docOriginal.Save(ArtifactsDir + "Revision.CompareOptions.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Comparing](../../aspose.words.comparing/)
* toplantı [Aspose.Words](../../)
