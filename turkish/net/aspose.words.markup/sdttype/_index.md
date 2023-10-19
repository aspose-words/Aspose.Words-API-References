---
title: SdtType Enum
linktitle: SdtType
articleTitle: SdtType
second_title: Aspose.Words for .NET
description: Aspose.Words.Markup.SdtType Sıralama. Yapılandırılmış belge etiketi SDT düğümünün türünü belirtir C#'da.
type: docs
weight: 4040
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
| None | `0` | SDT'ye hiçbir tür atanmadı. |
| Bibliography | `1` | SDT bir kaynakça girişini temsil eder. |
| Citation | `2` | SDT bir alıntıyı temsil eder. |
| Equation | `3` | SDT bir denklemi temsil eder. |
| DropDownList | `4` | SDT, belgede görüntülendiğinde bir açılır listeyi temsil eder. |
| ComboBox | `5` | SDT, belgede görüntülendiğinde bir birleşik giriş kutusunu temsil eder. |
| Date | `6` | SDT, belgede görüntülendiğinde bir tarih seçiciyi temsil eder. |
| BuildingBlockGallery | `7` | SDT, bir yapı taşı galeri türünü temsil eder. |
| DocPartObj | `8` | SDT, bir belge parçası türünü temsil eder. |
| Group | `9` | SDT, belgede görüntülendiğinde kısıtlı bir gruplamayı temsil eder. |
| Picture | `10` | SDT, belgede görüntülendiğinde bir resmi temsil eder. |
| RichText | `11` | SDT, belgede görüntülendiğinde zengin bir metin kutusunu temsil eder. |
| PlainText | `12` | SDT, belgede görüntülendiğinde düz bir metin kutusunu temsil eder. |
| Checkbox | `13` | SDT, belgede görüntülendiğinde bir onay kutusunu temsil eder. |
| RepeatingSection | `14` | SDT, belgede görüntülendiğinde yinelenen bölüm türünü temsil eder. |
| RepeatingSectionItem | `15` | SDT yinelenen bölüm öğesini temsil eder. |
| EntityPicker | `16` | SDT, kullanıcının harici içerik türünün bir örneğini seçmesine olanak tanıyan bir varlık seçiciyi temsil eder. |

## Örnekler

Satır düzeyinde grup yapılandırılmış belge etiketinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();

// Satır düzeyinde bir Grup yapılandırılmış belge etiketi oluşturun.
StructuredDocumentTag groupSdt = new StructuredDocumentTag(doc, SdtType.Group, MarkupLevel.Row);
table.AppendChild(groupSdt);
groupSdt.IsShowingPlaceholderText = false;
groupSdt.RemoveAllChildren();

// Yapılandırılmış belge etiketinin alt satırını oluşturun.
Row row = new Row(doc);
groupSdt.AppendChild(row);

Cell cell = new Cell(doc);
row.AppendChild(cell);

builder.EndTable();

// Hücre içeriğini ekleyin.
cell.EnsureMinimum();
builder.MoveTo(cell.LastParagraph);
builder.Write("Lorem ipsum dolor.");

//Tablodan sonra metni ekleyin.
builder.MoveTo(table.NextSibling);
builder.Write("Nulla blandit nisi.");

doc.Save(ArtifactsDir + "StructuredDocumentTag.SdtAtRowLevel.docx");
```

İçerik kontrol öğelerine ilişkin stillerle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda belgeden yapılandırılmış belge etiketine stil uygulamanın iki yolu verilmiştir.
// 1 - Belgenin stil koleksiyonundan bir stil nesnesi uygulayın:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Belgedeki bir stile ada göre referans verin:
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

Bir tablonun XML bölümündeki verilerle nasıl doldurulacağını gösterir.

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

// XML içeriğindeki veriler için başlıklar oluşturun.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Title");
builder.InsertCell();
builder.Write("Author");
builder.EndRow();
builder.EndTable();

// İçinde yinelenen bölüm bulunan bir tablo oluşturun.
StructuredDocumentTag repeatingSectionSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSection, MarkupLevel.Row);
repeatingSectionSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book", string.Empty);
table.AppendChild(repeatingSectionSdt);

// Yinelenen bölümün içine yinelenen bölüm öğesini ekleyin ve onu satır olarak işaretleyin.
// Bu tabloda XML belgesinde bulabileceğimiz her öğe için bir satır bulunacaktır
// "/books[1]/book" XPath'ı kullanarak, ki bunlardan üç tane var.
StructuredDocumentTag repeatingSectionItemSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSectionItem, MarkupLevel.Row);
repeatingSectionSdt.AppendChild(repeatingSectionItemSdt);

Row row = new Row(doc);
repeatingSectionItemSdt.AppendChild(row);

// XML verilerini her kitabın başlığı ve yazarı için oluşturulan tablo hücreleriyle eşleyin.
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
