---
title: Document.Compare
second_title: Aspose.Words for .NET API Referansı
description: Document yöntem. Bu belgeyi düzenleme ve biçim revizyonlarının sayısı olarak değişiklik üreten başka bir belgeyle karşılaştırırRevision .
type: docs
weight: 580
url: /tr/net/aspose.words/document/compare/
---
## Compare(Document, string, DateTime) {#compare}

Bu belgeyi, düzenleme ve biçim revizyonlarının sayısı olarak değişiklik üreten başka bir belgeyle karşılaştırır[`Revision`](../../revision/) .

```csharp
public void Compare(Document document, string author, DateTime dateTime)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| document | Document | Karşılaştırılacak belge. |
| author | String | Düzeltmelerde kullanılacak yazarın baş harfleri. |
| dateTime | DateTime | Düzeltmeler için kullanılacak tarih ve saat. |

### Notlar

Dokümanlarda karşılaştırma yapılmadan önce revizyon yapılmamalıdır.

### Örnekler

Belgelerin nasıl karşılaştırılacağını gösterir.

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// Dokümanların revizyonlarla karşılaştırılması bir istisna oluşturacaktır.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// Karşılaştırma sonrasında orijinal doküman yeni bir revizyona kavuşacak
// düzenlenen belgedeki farklı olan her öğe için.
foreach (Revision r in docOriginal.Revisions)
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// Bu revizyonların kabul edilmesi orijinal belgeyi düzenlenen belgeye dönüştürecektir.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)

---

## Compare(Document, string, DateTime, CompareOptions) {#compare_1}

Bu belgeyi, bir dizi düzenleme ve biçim revizyonu şeklinde değişiklik üreten başka bir belgeyle karşılaştırır[`Revision`](../../revision/) . Karşılaştırma seçeneklerini belirtmeye olanak sağlar.[`CompareOptions`](../../../aspose.words.comparing/compareoptions/) .

```csharp
public void Compare(Document document, string author, DateTime dateTime, CompareOptions options)
```

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

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)


