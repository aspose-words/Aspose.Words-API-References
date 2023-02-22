---
title: Class CompareOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Comparing.CompareOptions sınıf. Belge karşılaştırma işlemi için gelişmiş seçeneklerin seçilmesini sağlar.
type: docs
weight: 260
url: /tr/net/aspose.words.comparing/compareoptions/
---
## CompareOptions class

Belge karşılaştırma işlemi için gelişmiş seçeneklerin seçilmesini sağlar.

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
| [Granularity](../../aspose.words.comparing/compareoptions/granularity/) { get; set; } | Değişikliklerin karaktere göre mi yoksa kelimeye göre mi izlendiğini belirtir. Varsayılan değerWordLevel . |
| [IgnoreCaseChanges](../../aspose.words.comparing/compareoptions/ignorecasechanges/) { get; set; } | True, belge karşılaştırmasının büyük/küçük harfe duyarlı olmadığını gösterir. Varsayılan olarak karşılaştırma büyük/küçük harf duyarlıdır. |
| [IgnoreComments](../../aspose.words.comparing/compareoptions/ignorecomments/) { get; set; } | Yorumlardaki farklılıkların karşılaştırılıp karşılaştırılmayacağını belirtir. Varsayılan olarak yorumlar göz ardı edilmez. |
| [IgnoreDmlUniqueId](../../aspose.words.comparing/compareoptions/ignoredmluniqueid/) { get; set; } | DrawingML benzersiz kimliğindeki farkın yoksayılıp yoksayılmayacağını belirtir. Varsayılan değer **yanlış** . |
| [IgnoreFields](../../aspose.words.comparing/compareoptions/ignorefields/) { get; set; } | Alanlardaki farklılıkların karşılaştırılıp karşılaştırılmayacağını belirtir. Varsayılan olarak alanlar göz ardı edilmez. |
| [IgnoreFootnotes](../../aspose.words.comparing/compareoptions/ignorefootnotes/) { get; set; } | Dipnotlardaki ve son notlardaki farklılıkların karşılaştırılıp karşılaştırılmayacağını belirtir. Varsayılan olarak dipnotlar göz ardı edilmez. |
| [IgnoreFormatting](../../aspose.words.comparing/compareoptions/ignoreformatting/) { get; set; } | True, biçimlendirmenin yoksayıldığını gösterir. Varsayılan olarak belge biçimlendirmesi göz ardı edilmez. |
| [IgnoreHeadersAndFooters](../../aspose.words.comparing/compareoptions/ignoreheadersandfooters/) { get; set; } | True, üstbilgi ve altbilgi içeriğinin yok sayıldığını belirtir. Varsayılan olarak üstbilgiler ve altbilgiler yoksayılmaz. |
| [IgnoreTables](../../aspose.words.comparing/compareoptions/ignoretables/) { get; set; } | Tablolarda bulunan verilerdeki farklılıkların karşılaştırılıp karşılaştırılmayacağını belirtir. Varsayılan olarak tablolar göz ardı edilmez. |
| [IgnoreTextboxes](../../aspose.words.comparing/compareoptions/ignoretextboxes/) { get; set; } | Metin kutularında bulunan verilerdeki farklılıkların karşılaştırılıp karşılaştırılmayacağını belirtir. Varsayılan olarak metin kutuları göz ardı edilmez. |
| [Target](../../aspose.words.comparing/compareoptions/target/) { get; set; } | Karşılaştırma sırasında hedef olarak hangi belgenin kullanılacağını belirtir. |

### Örnekler

Karşılaştırma yaparken belirli türdeki belge öğelerinin nasıl filtreleneceğini gösterir.

```csharp
// Orijinal belgeyi oluşturun ve onu çeşitli öğelerle doldurun.
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);

// Son notla başvurulan paragraf metni:
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

// Belgemizin bir klonunu oluşturun ve klonlanan belgenin öğelerinin her biri üzerinde hızlı bir düzenleme yapın.
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
// Bir CompareOptions nesnesi, revizyonları bastırabilen bir dizi işarete sahiptir.
// her ilgili öğe türünde, değişikliklerini etkin bir şekilde yok sayar.
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


