---
title: Enum ComparisonTargetType
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Comparing.ComparisonTargetType Sıralama. Karşılaştırma sırasında kullanılacak temel belgenin belirtilmesine olanak tanır. Varsayılan değerCurrent .
type: docs
weight: 280
url: /tr/net/aspose.words.comparing/comparisontargettype/
---
## ComparisonTargetType enumeration

Karşılaştırma sırasında kullanılacak temel belgenin belirtilmesine olanak tanır. Varsayılan değer:Current .

```csharp
public enum ComparisonTargetType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Current | `0` | Bu belge karşılaştırma sırasında temel olarak kullanılır. |
| New | `1` | Karşılaştırma sırasında diğer belge temel olarak kullanılır. |

### Notlar

"Belgeleri Karşılaştır" iletişim kutusundaki Microsoft Word "Değişiklikleri göster" seçeneğiyle ilgilidir.

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


