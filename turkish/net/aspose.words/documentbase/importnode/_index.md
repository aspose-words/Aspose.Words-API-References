---
title: DocumentBase.ImportNode
second_title: Aspose.Words for .NET API Referansı
description: DocumentBase yöntem. Başka bir belgedeki bir düğümü geçerli belgeye aktarır.
type: docs
weight: 100
url: /tr/net/aspose.words/documentbase/importnode/
---
## ImportNode(Node, bool) {#importnode}

Başka bir belgedeki bir düğümü geçerli belgeye aktarır.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcNode | Node | İçe aktarılan düğüm. |
| isImportChildren | Boolean | `doğru` tüm alt düğümleri yinelemeli olarak içe aktarmak için; aksi takdirde,`YANLIŞ`. |

### Geri dönüş değeri

Geçerli belgeye ait klonlanmış düğüm.

### Notlar

Bu yöntem şunları kullanır:UseDestinationStyles biçimlendirmeyi çözme seçeneği.

Bir düğümün içe aktarılması, içe aktarılan belgeye ait kaynak düğümün bir kopyasını oluşturur. Döndürülen düğümün üst öğesi yok. Kaynak düğüm değiştirilmez veya orijinal belgeden kaldırılmaz.

Başka bir belgedeki bir düğümün bu belgeye eklenmeden önce içe aktarılması gerekir. İçe aktarma sırasında, stillere ve listelere yapılan referanslar gibi belgeye özgü özellikler orijinalden içe aktarılan belgeye çevrilir . Düğüm içe aktarıldıktan sonra, kullanılarak belgedeki uygun yere eklenebilir.Node) veya Node).

Kaynak düğüm zaten hedef belgeye aitse, kaynak düğümün derin clone 'si oluşturulur.

### Örnekler

Bir düğümün bir belgeden diğerine nasıl aktarılacağını gösterir.

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

srcDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(srcDoc, "Source document first paragraph text."));
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(dstDoc, "Destination document first paragraph text."));

// Her düğümün, düğümü içeren belge olan bir ana belgesi vardır.
// Düğümün ait olmadığı bir belgeye bir düğüm eklemek bir istisna oluşturacaktır.
Assert.AreNotEqual(dstDoc, srcDoc.FirstSection.Document);
Assert.Throws<ArgumentException>(() => { dstDoc.AppendChild(srcDoc.FirstSection); });

// Belgeyi içerecek bir düğümün kopyasını oluşturmak için ImportNode yöntemini kullanın
// yeni sahip belgesi olarak ImportNode yöntem kümesini çağıran.
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

Biçimlendirmeyi kontrol etme seçeneğiyle birlikte başka bir belgedeki bir düğümü geçerli belgeye aktarır.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren, ImportFormatMode importFormatMode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcNode | Node | İçe aktarılacak düğüm. |
| isImportChildren | Boolean | `doğru` tüm alt düğümleri yinelemeli olarak içe aktarmak için; aksi takdirde,`YANLIŞ`. |
| importFormatMode | ImportFormatMode | Çakışan stil formatlamasının nasıl birleştirileceğini belirtir. |

### Geri dönüş değeri

Klonlanmış, içe aktarılmış düğüm. Düğüm hedef belgeye aittir ancak üst öğesi yoktur.

### Notlar

Bu aşırı yükleme, stillerin ve liste formatının nasıl içe aktarıldığını kontrol etmek için kullanışlıdır.

Bir düğümün içe aktarılması, içe aktarılan belgeye ait kaynak düğümün bir kopyasını oluşturur. Döndürülen düğümün üst öğesi yok. Kaynak düğüm değiştirilmez veya orijinal belgeden kaldırılmaz.

Başka bir belgedeki bir düğümün bu belgeye eklenmeden önce içe aktarılması gerekir. İçe aktarma sırasında, stillere ve listelere yapılan referanslar gibi belgeye özgü özellikler orijinalden içe aktarılan belgeye çevrilir . Düğüm içe aktarıldıktan sonra, kullanılarak belgedeki uygun yere eklenebilir.Node) veya Node).

Kaynak düğüm zaten hedef belgeye aitse, kaynak düğümün derin clone 'si oluşturulur.

### Örnekler

Düğümün kaynak belgeden hedef belgeye belirli seçeneklerle nasıl aktarılacağını gösterir.

```csharp
// İki belge oluşturun ve her belgeye bir karakter stili ekleyin.
// Stilleri aynı ada ancak farklı metin formatına sahip olacak şekilde yapılandırın.
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

// Bölümü hedef belgeden kaynak belgeye aktararak stil adı çakışmasına neden olun.
// Hedef stilleri kullanırsak, aynı stil adına sahip içe aktarılan kaynak metin
// hedef metni hedef stilini benimseyecektir.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.UseDestinationStyles);
Assert.AreEqual(dstStyle.Font.Name, importedSection.Body.FirstParagraph.Runs[0].Font.Name);
Assert.AreEqual(dstStyle.Name, importedSection.Body.FirstParagraph.Runs[0].Font.StyleName);

// ImportFormatMode.KeepDifferentStyles kullanırsak kaynak stili korunur,
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


