---
title: Document.Compare
linktitle: Compare
articleTitle: Compare
second_title: .NET için Aspose.Words
description: Belgeleri Belge Karşılaştırma aracımızla zahmetsizce karşılaştırın. Düzenlemeleri ve biçim değişikliklerini hızlı bir şekilde belirleyerek, kolaylaştırılmış revizyonlar ve gelişmiş iş birliği sağlayın.
type: docs
weight: 600
url: /tr/net/aspose.words/document/compare/
---
## Compare(*[Document](../), string, DateTime*) {#compare}

Bu belgeyi düzenleme ve biçim revizyonlarının sayısı olarak değişiklik üreten başka bir belgeyle karşılaştırır[`Revision`](../../revision/) .

```csharp
public void Compare(Document document, string author, DateTime dateTime)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| document | Document | Karşılaştırılacak belge. |
| author | String | Revizyonlarda kullanılacak yazarın baş harfleri. |
| dateTime | DateTime | Revizyonlar için kullanılacak tarih ve saat. |

## Notlar

Karşılaştırma öncesinde dokümanlarda revizyon olmamalıdır.

## Örnekler

Belgelerin nasıl karşılaştırılacağını gösterir.

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// Revizyonlu belgeleri karşılaştırmak bir istisna oluşturacaktır.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// Karşılaştırmadan sonra orijinal belge yeni bir revizyon kazanacak
// düzenlenen belgede farklı olan her bir öğe için.
foreach (Revision r in docOriginal.Revisions)
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// Bu revizyonları kabul etmek, orijinal belgeyi düzenlenmiş belgeye dönüştürecektir.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Compare(*[Document](../), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_1}

Bu belgeyi başka bir belgeyle karşılaştırır ve bir dizi düzenleme ve biçim revizyonu olarak değişiklikler üretir[`Revision`](../../revision/) . Karşılaştırma seçeneklerini belirtmeye olanak tanır[`CompareOptions`](../../../aspose.words.comparing/compareoptions/) .

```csharp
public void Compare(Document document, string author, DateTime dateTime, CompareOptions options)
```

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

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
