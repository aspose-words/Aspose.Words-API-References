---
title: SectionCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: SectionCollection Item mülk. Verilen dizindeki bir bölümü alır C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words/sectioncollection/item/
---
## SectionCollection indexer

Verilen dizindeki bir bölümü alır.

```csharp
public Section this[int index] { get; }
```

| Parametre | Tanım |
| --- | --- |
| index | Bölüm listesine bir dizin. |

## Notlar

Endeks sıfır bazlıdır.

Negatif dizinlere izin verilir ve koleksiyonun arkasından erişimi belirtir. Örneğin -1 son öğe anlamına gelir, -2 sondan önceki ikinci öğe anlamına gelir ve bu şekilde devam eder.

Dizin listedeki öğe sayısından büyük veya ona eşitse bu, boş bir başvuru döndürür.

Dizin negatifse ve mutlak değeri listedeki öğe sayısından büyükse bu, boş bir başvuru döndürür.

## Örnekler

Belgenin sayfa düzeninin ne zaman yeniden hesaplanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Bir belgeyi PDF'ye veya görüntüye kaydetmek veya ilk kez yazdırmak otomatik olarak
// sayfalarının içindeki belgenin düzenini önbelleğe al.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Belgeyi bir şekilde değiştirin.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

 // Aspose.Words'ün mevcut sürümünde belgeyi değiştirmek otomatik olarak yeniden oluşturmuyor
// önbelleğe alınan sayfa düzeni. Önbelleğe alınmış düzeni istiyorsak
// güncel kalmak için manuel olarak güncellememiz gerekecek.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

Düzenleme için yeni bir bölüm düğümünün nasıl hazırlanacağını gösterir.

```csharp
Document doc = new Document();

// Boş bir belge, bir gövdeye sahip olan ve bunun da bir paragrafa sahip olduğu bir bölümle birlikte gelir.
// Bu paragrafa metin dizileri, şekiller veya tablolar gibi öğeler ekleyerek bu belgeye içerik ekleyebiliriz.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Bunun gibi yeni bir bölüm eklersek ne gövdesi ne de başka bir alt düğümü olmayacak.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Düzenlemeye başlamak için bu bölüme bir gövde ve paragraf eklemek üzere "EnsureMinimum" yöntemini çalıştırın.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [Section](../../section/)
* class [SectionCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
