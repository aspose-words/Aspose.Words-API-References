---
title: ImportNode
second_title: Aspose.Words for .NET API Referansı
description: Bir düğümü başka bir belgeden geçerli belgeye aktarır.
type: docs
weight: 100
url: /tr/net/aspose.words/documentbase/importnode/
---
## ImportNode(Node, bool) {#importnode}

Bir düğümü başka bir belgeden geçerli belgeye aktarır.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcNode | Node | Düğüm içe aktarılıyor. |
| isImportChildren | Boolean | Tüm alt düğümleri yinelemeli olarak içe aktarmak için doğru; aksi halde yanlış. |

### Geri dönüş değeri

Geçerli belgeye ait klonlanmış düğüm.

### Notlar

Bu yöntem,UseDestinationStyles biçimlendirmeyi çözme seçeneği.

Bir düğümü içe aktarmak, içe aktarma belgesine ait kaynak düğümün bir kopyasını oluşturur. Döndürülen düğümün üst öğesi yok. Kaynak düğüm değiştirilmez veya orijinal belgeden kaldırılmaz.

Başka bir belgeden bir düğüm bu belgeye eklenmeden önce içe aktarılmalıdır. İçe aktarma sırasında, stillere ve listelere referanslar gibi belgeye özgü özellikler orijinalden içe aktarılan belgeye çevrilir. Düğüm içe aktarıldıktan sonra, kullanılarak belgedeki uygun yere eklenebilir.[`InsertBefore`](../../compositenode/insertbefore/) veya [`InsertAfter`](../../compositenode/insertafter/).

Kaynak düğüm zaten hedef belgeye aitse, kaynak düğümün derin bir klonu oluşturulur.

### Örnekler

Bir düğümün bir belgeden diğerine nasıl aktarılacağını gösterir.

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

srcDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(srcDoc, "Source document first paragraph text."));
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(dstDoc, "Destination document first paragraph text."));

// Her düğümün, düğümü içeren belge olan bir üst belgesi vardır.
// Düğümün ait olmadığı bir belgeye bir düğüm eklemek bir istisna atar.
Assert.AreNotEqual(dstDoc, srcDoc.FirstSection.Document);
Assert.Throws<ArgumentException>(() => { dstDoc.AppendChild(srcDoc.FirstSection); });

// Belgeye sahip olacak bir düğümün kopyasını oluşturmak için ImportNode yöntemini kullanın
// yeni sahip belgesi olarak ayarlanmış ImportNode yöntemini çağıran.
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
* ad alanı [Aspose.Words](../../documentbase/)
* toplantı [Aspose.Words](../../../)

---

## ImportNode(Node, bool, ImportFormatMode) {#importnode_1}

Biçimlendirmeyi kontrol etme seçeneği ile bir düğümü başka bir belgeden geçerli belgeye aktarır.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren, ImportFormatMode importFormatMode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcNode | Node | İçe aktarılacak düğüm. |
| isImportChildren | Boolean | Tüm alt düğümleri yinelemeli olarak içe aktarmak için doğru; aksi halde yanlış. |
| importFormatMode | ImportFormatMode | Çakışan stil biçimlendirmesinin nasıl birleştirileceğini belirtir. |

### Geri dönüş değeri

Klonlanmış, içe aktarılan düğüm. Düğüm, hedef belgeye aittir, ancak üst öğesi yoktur.

### Notlar

Bu aşırı yükleme, stillerin ve liste biçimlendirmesinin nasıl içe aktarıldığını kontrol etmek için kullanışlıdır.

Bir düğümü içe aktarmak, içe aktarma belgesine ait kaynak düğümün bir kopyasını oluşturur. Döndürülen düğümün üst öğesi yok. Kaynak düğüm değiştirilmez veya orijinal belgeden kaldırılmaz.

Başka bir belgeden bir düğüm bu belgeye eklenmeden önce içe aktarılmalıdır. İçe aktarma sırasında, stillere ve listelere referanslar gibi belgeye özgü özellikler orijinalden içe aktarılan belgeye çevrilir. Düğüm içe aktarıldıktan sonra, kullanılarak belgedeki uygun yere eklenebilir.[`InsertBefore`](../../compositenode/insertbefore/) veya [`InsertAfter`](../../compositenode/insertafter/).

Kaynak düğüm zaten hedef belgeye aitse, kaynak düğümün derin bir klonu oluşturulur.

### Örnekler

Belirli seçeneklerle düğümün kaynak belgeden hedef belgeye nasıl aktarılacağını gösterir.

```csharp
// İki belge oluşturun ve her belgeye bir karakter stili ekleyin.
// Stilleri aynı ada, ancak farklı metin biçimlendirmesine sahip olacak şekilde yapılandırın.
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

// Bölüm'ü hedef belgeden kaynak belgeye aktararak stil adı çakışmasına neden olur.
// Hedef stilleri kullanırsak, aynı stil adına sahip içe aktarılan kaynak metin
// hedef metin olarak hedef stili benimser.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.UseDestinationStyles);
Assert.AreEqual(dstStyle.Font.Name, importedSection.Body.FirstParagraph.Runs[0].Font.Name);
Assert.AreEqual(dstStyle.Name, importedSection.Body.FirstParagraph.Runs[0].Font.StyleName);

// ImportFormatMode.KeepDifferentStyles kullanırsak, kaynak stil korunur,
// ve adlandırma çakışması bir sonek eklenerek çözülür.
dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.KeepDifferentStyles);
Assert.AreEqual(dstStyle.Font.Name, dstDoc.Styles["My style"].Font.Name);
Assert.AreEqual(srcStyle.Font.Name, dstDoc.Styles["My style_0"].Font.Name);
```

### Ayrıca bakınız

* class [Node](../../node/)
* enum [ImportFormatMode](../../importformatmode/)
* class [DocumentBase](../)
* ad alanı [Aspose.Words](../../documentbase/)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
