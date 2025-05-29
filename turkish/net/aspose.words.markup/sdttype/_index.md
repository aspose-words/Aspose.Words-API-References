---
title: SdtType Enum
linktitle: SdtType
articleTitle: SdtType
second_title: .NET için Aspose.Words
description: Gelişmiş belge yönetimi ve sorunsuz iş akışları için yapılandırılmış belge etiketi türlerini tanımlayan Aspose.Words.Markup.SdtType enum'unu keşfedin.
type: docs
weight: 4730
url: /tr/net/aspose.words.markup/sdttype/
---
## SdtType enumeration

Yapılandırılmış belge etiketi (SDT) düğümünün türünü belirtir.

```csharp
public enum SdtType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | SDT'ye hiçbir tür atanmamıştır. |
| Bibliography | `1` | SDT bir bibliyografya girişini temsil eder. |
| Citation | `2` | SDT bir atıfı temsil eder. |
| Equation | `3` | SDT bir denklemi temsil eder. |
| DropDownList | `4` | SDT, belgede görüntülendiğinde bir açılır listeyi temsil eder. |
| ComboBox | `5` | SDT, belgede görüntülendiğinde bir birleşik kutuyu temsil eder. |
| Date | `6` | SDT, belgede görüntülendiğinde bir tarih seçiciyi temsil eder. |
| BuildingBlockGallery | `7` | SDT bir yapı bloğu galerisi türünü temsil eder. |
| DocPartObj | `8` | SDT bir belge parçası türünü temsil eder. |
| Group | `9` | SDT, belgede görüntülendiğinde kısıtlı bir gruplamayı temsil eder. |
| Picture | `10` | SDT, belgede görüntülendiğinde bir resmi temsil eder. |
| RichText | `11` | SDT, belgede görüntülendiğinde zengin bir metin kutusunu temsil eder. |
| PlainText | `12` | SDT, belgede görüntülendiğinde düz metin kutusunu temsil eder. |
| Checkbox | `13` | SDT, belgede görüntülendiğinde bir onay kutusunu temsil eder. |
| RepeatingSection | `14` | SDT, belgede görüntülendiğinde tekrarlayan bölüm türünü temsil eder. |
| RepeatingSectionItem | `15` | SDT tekrar eden bölüm öğesini temsil eder. |
| EntityPicker | `16` | SDT, kullanıcının harici bir içerik türünün bir örneğini seçmesine olanak tanıyan bir varlık seçiciyi temsil eder. |

## Örnekler

Citation türünde yapılandırılmış bir belge etiketinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

StructuredDocumentTag sdt = new StructuredDocumentTag(doc, SdtType.Citation, MarkupLevel.Inline);
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
paragraph.AppendChild(sdt);

// Bir Alıntı alanı oluşturun.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToParagraph(0, -1);
builder.InsertField(@"CITATION Ath22 \l 1033 ", "(John Lennon, 2022)");

// Alanı yapılandırılmış belge etiketine taşı.
while (sdt.NextSibling != null)
    sdt.AppendChild(sdt.NextSibling);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Citation.docx");
```

Satır düzeyinde grup yapılandırılmış belge etiketinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();

// Satır düzeyinde Grup yapılandırılmış belge etiketi oluşturun.
StructuredDocumentTag groupSdt = new StructuredDocumentTag(doc, SdtType.Group, MarkupLevel.Row);
table.AppendChild(groupSdt);
groupSdt.IsShowingPlaceholderText = false;
groupSdt.RemoveAllChildren();

// Yapılandırılmış belge etiketinin bir alt satırını oluştur.
Row row = new Row(doc);
groupSdt.AppendChild(row);

Cell cell = new Cell(doc);
row.AppendChild(cell);

builder.EndTable();

// Hücre içeriğini ekle.
cell.EnsureMinimum();
builder.MoveTo(cell.LastParagraph);
builder.Write("Lorem ipsum dolor.");

// Tablodan sonra metin ekle.
builder.MoveTo(table.NextSibling);
builder.Write("Nulla blandit nisi.");

doc.Save(ArtifactsDir + "StructuredDocumentTag.SdtAtRowLevel.docx");
```

İçerik kontrol öğeleri için stillerle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda, bir belgeden yapılandırılmış belge etiketine bir stil uygulamanın iki yolu bulunmaktadır.
// 1 - Belgenin stil koleksiyonundan bir stil nesnesi uygula:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Belgedeki bir stile adıyla başvuruda bulunun:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Console.WriteLine(sdt.WordOpenXMLMinimal);

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

XML parçasındaki verilerle bir tablonun nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

CustomXmlPart xmlPart = doc.CustomXmlParts.Add("Books",
    "<books>" +
        "<book>" +
            "<title>Everyday Italian</title>" +
            "<author>Giada De Laurentiis</author>" +
        "</book>" +
        "<book>" +
            "<title>The C Programming Language</title>" +
            "<author>Brian W. Kernighan, Dennis M. Ritchie</author>" +
        "</book>" +
        "<book>" +
            "<title>Learning XML</title>" +
            "<author>Erik T. Ray</author>" +
        "</book>" +
    "</books>");

// XML içeriğinden veriler için başlıklar oluşturun.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Title");
builder.InsertCell();
builder.Write("Author");
builder.EndRow();
builder.EndTable();

// İçerisinde tekrar eden bir bölüm bulunan bir tablo oluştur.
StructuredDocumentTag repeatingSectionSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSection, MarkupLevel.Row);
repeatingSectionSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book", string.Empty);
table.AppendChild(repeatingSectionSdt);

// Tekrarlanan bölümün içine tekrarlanan bölüm öğesi ekle ve bunu bir satır olarak işaretle.
// Bu tablo, XML belgesinde bulabileceğimiz her bir öğe için bir satıra sahip olacak
// Üç tane olan "/books[1]/book" XPath'sini kullanarak.
StructuredDocumentTag repeatingSectionItemSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSectionItem, MarkupLevel.Row);
repeatingSectionSdt.AppendChild(repeatingSectionItemSdt);

Row row = new Row(doc);
repeatingSectionItemSdt.AppendChild(row);

// Her kitabın başlığı ve yazarı için oluşturulan tablo hücreleriyle XML verilerini eşle.
StructuredDocumentTag titleSdt =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Cell);
titleSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book[1]/title[1]", string.Empty);
row.AppendChild(titleSdt);

StructuredDocumentTag authorSdt =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Cell);
authorSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book[1]/author[1]", string.Empty);
row.AppendChild(authorSdt);

doc.Save(ArtifactsDir + "StructuredDocumentTag.RepeatingSectionItem.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)
