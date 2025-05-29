---
title: StructuredDocumentTagRangeStart
linktitle: StructuredDocumentTagRangeStart
articleTitle: StructuredDocumentTagRangeStart
second_title: .NET için Aspose.Words
description: Zahmetsizce yeni bir StructuredDocumentTagRangeStart örneği oluşturun. Yapılandırılmış etiketler için bu güçlü oluşturucuyla belge yönetiminizi geliştirin.
type: docs
weight: 10
url: /tr/net/aspose.words.markup/structureddocumenttagrangestart/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart constructor

Yeni bir örneğini başlatır**Yapılandırılmış belge etiketi aralığı başlangıcı** sınıf.

```csharp
public StructuredDocumentTagRangeStart(DocumentBase doc, SdtType type)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | DocumentBase | Sahip belgesi. |
| type | SdtType | SDT düğümünün türü. |

## Notlar

Aşağıdaki SDT türleri oluşturulabilir:

* Checkbox
* DropDownList
* ComboBox
* Date
* BuildingBlockGallery
* Group
* Picture
* RichText
* PlainText

## Örnekler

Yapılandırılmış belge etiketinin ve içeriğinin nasıl oluşturulacağını/kaldırılacağını gösterir.

```csharp
public void SdtRangeExtendedMethods()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("StructuredDocumentTag element");

    StructuredDocumentTagRangeStart rangeStart = InsertStructuredDocumentTagRanges(doc);

    // Aralıklı yapılandırılmış belge etiketini kaldırır, ancak içeriği içeride tutar.
    rangeStart.RemoveSelfOnly();

    rangeStart = (StructuredDocumentTagRangeStart)doc.GetChild(
        NodeType.StructuredDocumentTagRangeStart, 0, false);
    Assert.AreEqual(null, rangeStart);

    StructuredDocumentTagRangeEnd rangeEnd = (StructuredDocumentTagRangeEnd)doc.GetChild(
        NodeType.StructuredDocumentTagRangeEnd, 0, false);

    Assert.AreEqual(null, rangeEnd);
    Assert.AreEqual("StructuredDocumentTag element", doc.GetText().Trim());

    rangeStart = InsertStructuredDocumentTagRanges(doc);

    Node paragraphNode = rangeStart.LastOrDefault();
    Assert.AreEqual("StructuredDocumentTag element", paragraphNode?.GetText().Trim());

    // Aralıklı yapılandırılmış belge etiketini ve içindeki içeriği kaldırır.
    rangeStart.RemoveAllChildren();

    paragraphNode = rangeStart.LastOrDefault();
    Assert.AreEqual(null, paragraphNode?.GetText());
}

public StructuredDocumentTagRangeStart InsertStructuredDocumentTagRanges(Document doc)
{
    StructuredDocumentTagRangeStart rangeStart = new StructuredDocumentTagRangeStart(doc, SdtType.PlainText);
    StructuredDocumentTagRangeEnd rangeEnd = new StructuredDocumentTagRangeEnd(doc, rangeStart.Id);

    doc.FirstSection.Body.InsertBefore(rangeStart, doc.FirstSection.Body.FirstParagraph);
    doc.LastSection.Body.InsertAfter(rangeEnd, doc.FirstSection.Body.FirstParagraph);

    return rangeStart;
}
```

### Ayrıca bakınız

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [SdtType](../../sdttype/)
* class [StructuredDocumentTagRangeStart](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
