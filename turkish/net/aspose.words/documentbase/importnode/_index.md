---
title: DocumentBase.ImportNode
linktitle: ImportNode
articleTitle: ImportNode
second_title: .NET için Aspose.Words
description: İş akışınızı DocumentBase'in ImportNode yöntemi ile geliştirmek için diğer belgelerden düğümleri zahmetsizce içe aktarın. Belge yönetiminizi bugün kolaylaştırın!
type: docs
weight: 110
url: /tr/net/aspose.words/documentbase/importnode/
---
## ImportNode(*[Node](../../node/), bool*) {#importnode}

Başka bir belgeden bir düğümü geçerli belgeye aktarır.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcNode | Node | İçeri aktarılan düğüm. |
| isImportChildren | Boolean | `doğru` tüm alt düğümleri yinelemeli olarak içe aktarmak için; aksi takdirde,`YANLIŞ`. |

### Geri dönüş değeri

Geçerli belgeye ait klonlanmış düğüm.

## Notlar

Bu yöntem şunu kullanır:UseDestinationStyles Biçimlendirmeyi çözme seçeneği.

Bir düğümü içe aktarmak, içe aktarılan belgeye ait kaynak düğümün bir kopyasını oluşturur. Döndürülen düğümün üst öğesi yoktur. Kaynak düğüm orijinal belgeden değiştirilmez veya kaldırılmaz.

Başka bir belgeden bir düğüm bu belgeye eklenmeden önce içe aktarılmalıdır. İçe aktarma sırasında, stillere ve listelere referanslar gibi belgeye özgü özellikler orijinalden içe aktarılan belgeye çevrilir. Düğüm içe aktarıldıktan sonra, belgedeki uygun yere şu şekilde eklenebilir: [`InsertBefore`](../../compositenode/insertbefore/) veya [`InsertAfter`](../../compositenode/insertafter/).

Kaynak düğüm zaten hedef belgeye aitse, o zaman kaynak düğümün basitçe derin bir clone 'si oluşturulur.

## Örnekler

Bir düğümün bir belgeden diğerine nasıl aktarılacağını gösterir.

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

srcDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(srcDoc, "Source document first paragraph text."));
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(dstDoc, "Destination document first paragraph text."));

// Her düğümün, düğümü içeren belge olan bir üst belgesi vardır.
// Bir düğümün ait olmadığı bir belgeye eklenmesi bir istisna fırlatacaktır.
Assert.AreNotEqual(dstDoc, srcDoc.FirstSection.Document);
Assert.Throws<ArgumentException>(() => dstDoc.AppendChild(srcDoc.FirstSection));

// Belgeyi içerecek bir düğümün kopyasını oluşturmak için ImportNode yöntemini kullanın
// ImportNode metodunu çağıran ve yeni sahibi olarak belgeyi ayarlayan.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true);

Assert.AreEqual(dstDoc, importedSection.Document);

// Artık düğümü belgeye ekleyebiliriz.
dstDoc.AppendChild(importedSection);

Assert.AreEqual("Destination document first paragraph text.\r\nSource document first paragraph text.\r\n",
    dstDoc.ToString(SaveFormat.Text));
```

### Ayrıca bakınız

* class [Node](../../node/)
* class [DocumentBase](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## ImportNode(*[Node](../../node/), bool, [ImportFormatMode](../../importformatmode/)*) {#importnode_1}

Biçimlendirmeyi kontrol etme seçeneğiyle başka bir belgeden geçerli belgeye bir düğüm aktarır.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren, ImportFormatMode importFormatMode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcNode | Node | İçe aktarılacak düğüm. |
| isImportChildren | Boolean | `doğru` tüm alt düğümleri yinelemeli olarak içe aktarmak için; aksi takdirde,`YANLIŞ`. |
| importFormatMode | ImportFormatMode | Çakışan stil biçimlendirmesinin nasıl birleştirileceğini belirtir. |

### Geri dönüş değeri

Klonlanmış, içe aktarılmış düğüm. Düğüm hedef belgeye aittir, ancak üst öğesi yoktur.

## Notlar

Bu aşırı yükleme, stillerin ve liste biçimlendirmesinin nasıl içe aktarılacağını kontrol etmek için yararlıdır.

Bir düğümü içe aktarmak, içe aktarılan belgeye ait kaynak düğümün bir kopyasını oluşturur. Döndürülen düğümün üst öğesi yoktur. Kaynak düğüm orijinal belgeden değiştirilmez veya kaldırılmaz.

Başka bir belgeden bir düğüm bu belgeye eklenmeden önce içe aktarılmalıdır. İçe aktarma sırasında, stillere ve listelere referanslar gibi belgeye özgü özellikler orijinalden içe aktarılan belgeye çevrilir. Düğüm içe aktarıldıktan sonra, belgedeki uygun yere şu şekilde eklenebilir: [`InsertBefore`](../../compositenode/insertbefore/) veya [`InsertAfter`](../../compositenode/insertafter/).

Kaynak düğüm zaten hedef belgeye aitse, o zaman kaynak düğümün basitçe derin bir clone 'si oluşturulur.

## Örnekler

Belirli seçeneklerle kaynak belgeden hedef belgeye düğümün nasıl aktarılacağını gösterir.

```csharp
// İki belge oluşturun ve her belgeye bir karakter stili ekleyin.
// Stilleri aynı ada sahip olacak şekilde, ancak farklı metin biçimlendirmesine sahip olacak şekilde yapılandırın.
Document srcDoc = new Document();
Style srcStyle = srcDoc.Styles.Add(StyleType.Character, "My style");
srcStyle.Font.Name = "Courier New";
DocumentBuilder srcBuilder = new DocumentBuilder(srcDoc);
srcBuilder.Font.Style = srcStyle;
srcBuilder.Writeln("Source document text.");

Document dstDoc = new Document();
Style dstStyle = dstDoc.Styles.Add(StyleType.Character, "My style");
dstStyle.Font.Name = "Calibri";
DocumentBuilder dstBuilder = new DocumentBuilder(dstDoc);
dstBuilder.Font.Style = dstStyle;
dstBuilder.Writeln("Destination document text.");

// Bölümü hedef belgeden kaynak belgeye aktarın, bu da stil adı çakışmasına neden olur.
// Hedef stilleri kullanırsak, aynı stil adına sahip içe aktarılan kaynak metin
// hedef metin hedef stilini benimseyecektir.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.UseDestinationStyles);
Assert.AreEqual(dstStyle.Font.Name, importedSection.Body.FirstParagraph.Runs[0].Font.Name);
Assert.AreEqual(dstStyle.Name, importedSection.Body.FirstParagraph.Runs[0].Font.StyleName);

// ImportFormatMode.KeepDifferentStyles'ı kullanırsak, kaynak stil korunur,
// ve isimlendirme çakışması bir sonek eklenerek çözülür.
dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.KeepDifferentStyles);
Assert.AreEqual(dstStyle.Font.Name, dstDoc.Styles["My style"].Font.Name);
Assert.AreEqual(srcStyle.Font.Name, dstDoc.Styles["My style_0"].Font.Name);
```

### Ayrıca bakınız

* class [Node](../../node/)
* enum [ImportFormatMode](../../importformatmode/)
* class [DocumentBase](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
