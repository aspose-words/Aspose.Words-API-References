---
title: CompareOptions.IgnoreHeadersAndFooters
linktitle: IgnoreHeadersAndFooters
articleTitle: IgnoreHeadersAndFooters
second_title: .NET için Aspose.Words
description: CompareOptions IgnoreHeadersAndFooters özelliğinin, daha temiz veri analizi için üst bilgileri ve alt bilgileri yok sayarak belge işlemeyi nasıl geliştirdiğini keşfedin.
type: docs
weight: 100
url: /tr/net/aspose.words.comparing/compareoptions/ignoreheadersandfooters/
---
## CompareOptions.IgnoreHeadersAndFooters property

True, başlık ve altbilgi içeriğinin göz ardı edildiğini gösterir.

```csharp
public bool IgnoreHeadersAndFooters { get; set; }
```

## Notlar

Varsayılan olarak başlıklar ve altbilgiler göz ardı edilmez.

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

* class [CompareOptions](../)
* ad alanı [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* toplantı [Aspose.Words](../../../)
