---
title: Class CompareOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Comparing.CompareOptions sınıf. Belge karşılaştırma işlemi için gelişmiş seçeneklerin seçilmesine olanak tanır.
type: docs
weight: 270
url: /tr/net/aspose.words.comparing/compareoptions/
---
## CompareOptions class

Belge karşılaştırma işlemi için gelişmiş seçeneklerin seçilmesine olanak tanır.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Belgeleri Karşılaştır](https://docs.aspose.com/words/net/compare-documents/) dokümantasyon makalesi.

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
| [CompareMoves](../../aspose.words.comparing/compareoptions/comparemoves/) { get; set; } | Farklılıkların karşılaştırılıp karşılaştırılmayacağını belirtir.MoveRevision iki belge arasında. Varsayılan olarak taşıma revizyonları üretilmez. |
| [Granularity](../../aspose.words.comparing/compareoptions/granularity/) { get; set; } | Değişikliklerin karaktere göre mi yoksa kelimeye göre mi izleneceğini belirtir. Varsayılan değer:WordLevel . |
| [IgnoreCaseChanges](../../aspose.words.comparing/compareoptions/ignorecasechanges/) { get; set; } | True, belge karşılaştırmasının büyük/küçük harfe duyarlı olmadığını belirtir. Karşılaştırma varsayılan olarak büyük/küçük harfe duyarlıdır. |
| [IgnoreComments](../../aspose.words.comparing/compareoptions/ignorecomments/) { get; set; } | Yorumlardaki farklılıkların karşılaştırılıp karşılaştırılmayacağını belirtir. Varsayılan olarak yorumlar dikkate alınmaz. |
| [IgnoreDmlUniqueId](../../aspose.words.comparing/compareoptions/ignoredmluniqueid/) { get; set; } | DrawingML benzersiz kimliğindeki farkın göz ardı edilip edilmeyeceğini belirtir. Varsayılan değer:`YANLIŞ` . |
| [IgnoreFields](../../aspose.words.comparing/compareoptions/ignorefields/) { get; set; } | Alanlardaki farklılıkların karşılaştırılıp karşılaştırılmayacağını belirtir. Varsayılan olarak alanlar göz ardı edilmez. |
| [IgnoreFootnotes](../../aspose.words.comparing/compareoptions/ignorefootnotes/) { get; set; } | Dipnot ve sonnotlardaki farklılıkların karşılaştırılıp karşılaştırılmayacağını belirtir. Varsayılan olarak dipnotlar göz ardı edilmez. |
| [IgnoreFormatting](../../aspose.words.comparing/compareoptions/ignoreformatting/) { get; set; } | Doğru, biçimlendirmenin göz ardı edildiğini gösterir. Varsayılan olarak belge biçimlendirmesi göz ardı edilmez. |
| [IgnoreHeadersAndFooters](../../aspose.words.comparing/compareoptions/ignoreheadersandfooters/) { get; set; } | Doğru, üstbilgi ve altbilgi içeriğinin göz ardı edildiğini belirtir. Varsayılan olarak üstbilgi ve altbilgiler göz ardı edilmez. |
| [IgnoreTables](../../aspose.words.comparing/compareoptions/ignoretables/) { get; set; } | Tablolarda bulunan verilerdeki farklılıkların karşılaştırılıp karşılaştırılmayacağını belirtir. Varsayılan olarak tablolar göz ardı edilmez. |
| [IgnoreTextboxes](../../aspose.words.comparing/compareoptions/ignoretextboxes/) { get; set; } | Metin kutularının içerdiği verilerdeki farklılıkların karşılaştırılıp karşılaştırılmayacağını belirtir. Varsayılan olarak metin kutuları göz ardı edilmez. |
| [Target](../../aspose.words.comparing/compareoptions/target/) { get; set; } | Karşılaştırma sırasında hangi belgenin hedef olarak kullanılacağını belirtir. |

### Örnekler

Karşılaştırma yaparken belirli belge öğesi türlerinin nasıl filtreleneceğini gösterir.

```csharp
// Orijinal belgeyi oluşturun ve onu çeşitli türde öğelerle doldurun.
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);

// Son notla referans verilen paragraf metni:
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

// Belgemizin bir kopyasını oluşturun ve kopyalanan belgenin her bir öğesi üzerinde hızlı bir düzenleme yapın.
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

// Belgelerin karşılaştırılması, düzenlenen belgedeki her düzenleme için bir revizyon oluşturur.
// CompareOptions nesnesinde revizyonları bastırabilecek bir dizi bayrak bulunur
// ilgili her öğe türü üzerinde, değişikliklerini etkili bir şekilde göz ardı ederek.
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.IgnoreFormatting = false;
compareOptions.IgnoreCaseChanges = false;
compareOptions.IgnoreComments = false;
compareOptions.IgnoreTables = false;
compareOptions.IgnoreFields = false;
compareOptions.IgnoreFootnotes = false;
compareOptions.IgnoreTextboxes = false;
compareOptions.IgnoreHeadersAndFooters = false;
compareOptions.Target = ComparisonTargetType.New;

docOriginal.Compare(docEdited, "John Doe", DateTime.Now, compareOptions);
docOriginal.Save(ArtifactsDir + "Document.CompareOptions.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Comparing](../../aspose.words.comparing/)
* toplantı [Aspose.Words](../../)


