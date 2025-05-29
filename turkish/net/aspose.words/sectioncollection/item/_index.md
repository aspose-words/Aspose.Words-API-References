---
title: SectionCollection.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: SectionCollection Item özelliğiyle belirli bölümlere zahmetsizce erişin. Kolaylaştırılmış veri yönetimi için herhangi bir bölümü dizine göre alın.
type: docs
weight: 10
url: /tr/net/aspose.words/sectioncollection/item/
---
## SectionCollection indexer

Belirtilen dizindeki bir bölümü alır.

```csharp
public Section this[int index] { get; }
```

| Parametre | Tanım |
| --- | --- |
| index | Bölümlerin listesine ait bir indeks. |

## Notlar

Endeks sıfır bazlıdır.

Negatif indekslere izin verilir ve koleksiyonun sonundan erişimi belirtir. Örneğin -1 son öğeyi, -2 sondan bir önceki öğeyi vb. ifade eder.

Eğer indeks listedeki öğe sayısından büyük veya eşitse, bu boş bir referans döndürür.

Eğer indeks negatifse ve mutlak değeri listedeki öğe sayısından büyükse, bu durum boş bir referans döndürür.

## Örnekler

Belgenin sayfa düzeninin ne zaman yeniden hesaplanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Bir belgeyi PDF'e, görüntüye kaydetmek veya ilk kez yazdırmak otomatik olarak
// Belgenin düzenini sayfalarının içinde önbelleğe al.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Belgeyi bir şekilde değiştirin.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// Aspose.Words'ün geçerli sürümünde, belgeyi değiştirmek otomatik olarak yeniden oluşturmaz
// önbelleğe alınmış sayfa düzeni. Önbelleğe alınmış düzeni istiyorsak
// Güncel kalmak için manuel olarak güncellememiz gerekecek.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

Yeni bir bölüm düğümünün düzenlemeye nasıl hazırlanacağını gösterir.

```csharp
Document doc = new Document();

// Boş bir belge, bir gövdeye sahip bir bölüm ve gövdenin de bir paragrafı ile birlikte gelir.
// Bu paragrafa metin bölümleri, şekiller veya tablolar gibi öğeler ekleyerek belgeye içerik ekleyebiliriz.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Eğer bu şekilde yeni bir bölüm eklersek, bir gövdesi veya başka herhangi bir alt düğümü olmayacaktır.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Bu bölümü düzenlemeye başlamak için "EnsureMinimum" metodunu çalıştırarak bir gövde ve bir paragraf ekleyin.
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
