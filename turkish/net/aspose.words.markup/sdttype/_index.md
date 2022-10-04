---
title: SdtType
second_title: Aspose.Words for .NET API Referansı
description: Yapılandırılmış belge etiketi SDT düğümünün türünü belirtir.
type: docs
weight: 3800
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
| None | `0` | SDT'ye hiçbir tür atanmamış. |
| Bibliography | `1` | SDT, bir kaynakça girişini temsil eder. |
| Citation | `2` | SDT bir alıntıyı temsil eder. |
| Equation | `3` | SDT bir denklemi temsil eder. |
| DropDownList | `4` | SDT, belgede görüntülendiğinde bir açılır listeyi temsil eder. |
| ComboBox | `5` | SDT, belgede görüntülendiğinde bir birleşik giriş kutusunu temsil eder. |
| Date | `6` | SDT, belgede görüntülendiğinde bir tarih seçiciyi temsil eder. |
| BuildingBlockGallery | `7` | SDT, bir yapı taşı galeri türünü temsil eder. |
| DocPartObj | `8` | SDT, bir belge parçası türünü temsil eder. |
| Group | `9` | SDT, belgede görüntülendiğinde sınırlı bir gruplamayı temsil eder. |
| Picture | `10` | SDT, belgede görüntülendiğinde bir resmi temsil eder. |
| RichText | `11` | SDT, belgede görüntülendiğinde zengin bir metin kutusunu temsil eder. |
| PlainText | `12` | SDT, belgede görüntülendiğinde bir düz metin kutusunu temsil eder. |
| Checkbox | `13` | SDT, belgede görüntülendiğinde bir onay kutusunu temsil eder. |
| RepeatingSection | `14` | SDT, belgede görüntülendiğinde yinelenen bölüm türünü temsil eder. |
| RepeatingSectionItem | `15` | SDT, yinelenen bölüm öğesini temsil eder. |
| EntityPicker | `16` | SDT, kullanıcının harici içerik türünün bir örneğini seçmesine izin veren bir varlık seçiciyi temsil eder. |

### Örnekler

İçerik kontrol öğeleri için stiller ile nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda, belgeden yapılandırılmış bir belge etiketine bir stil uygulamanın iki yolu verilmiştir.
// 1 - Belgenin stil koleksiyonundan bir stil nesnesi uygulayın:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Belgedeki bir stile ada göre başvuru yapın:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

Bir XML bölümündeki verilerle bir tablonun nasıl doldurulacağını gösterir.

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

// İçinde yinelenen bölüm olan bir tablo oluşturun.
StructuredDocumentTag repeatingSectionSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSection, MarkupLevel.Row);
repeatingSectionSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book", string.Empty);
table.AppendChild(repeatingSectionSdt);

// Yinelenen bölümün içine yinelenen bölüm öğesini ekleyin ve bir satır olarak işaretleyin.
// Bu tablo, XML belgesinde bulabileceğimiz her öğe için bir satıra sahip olacak
// üç tane olan "/books[1]/book" XPath kullanılarak.
StructuredDocumentTag repeatingSectionItemSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSectionItem, MarkupLevel.Row);
repeatingSectionSdt.AppendChild(repeatingSectionItemSdt);

Row row = new Row(doc);
repeatingSectionItemSdt.AppendChild(row);

// Her kitabın başlığı ve yazarı için oluşturulan tablo hücreleriyle XML verilerini eşleyin.
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
