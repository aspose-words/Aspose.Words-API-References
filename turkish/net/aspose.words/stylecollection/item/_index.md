---
title: StyleCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: StyleCollection Item mülk. Ada veya takma ada göre bir stil alır C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words/stylecollection/item/
---
## StyleCollection indexer (1 of 3)

Ada veya takma ada göre bir stil alır.

```csharp
public Style this[string name] { get; }
```

## Notlar

Büyük/küçük harfe duyarlı, döndürür`hükümsüz` verilen ada sahip stil bulunamazsa.

Bu, henüz mevcut olmayan yerleşik bir stilin İngilizce adıysa, onu otomatik olarak oluşturur.

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

### Ayrıca bakınız

* class [Style](../../style/)
* class [StyleCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## StyleCollection indexer (2 of 3)

Yerel ayardan bağımsız tanımlayıcıya göre yerleşik bir stil elde eder.

```csharp
public Style this[StyleIdentifier sti] { get; }
```

| Parametre | Tanım |
| --- | --- |
| sti | A[`StyleIdentifier`](../../styleidentifier/) Alınacak yerleşik stili belirten değer. |

## Notlar

Henüz var olmayan bir stile erişildiğinde, onu otomatik olarak oluşturur.

## Örnekler

Bir belgenin stil koleksiyonuna nasıl Stil ekleneceğini gösterir.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Daha sonra bu koleksiyona ekleyebileceğimiz yeni stiller için varsayılan parametreleri ayarlayın.
styles.DefaultFont.Name = "Courier New";
// "StyleType.Paragraph" stilini eklersek koleksiyon şu değerleri uygulayacaktır:
// "DefaultParagraphFormat" özelliğini stilin "ParagraphFormat" özelliğine dönüştürüyoruz.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Bir stil ekleyin ve ardından bunun varsayılan ayarlara sahip olduğunu doğrulayın.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Ayrıca bakınız

* class [Style](../../style/)
* enum [StyleIdentifier](../../styleidentifier/)
* class [StyleCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## StyleCollection indexer (3 of 3)

Dizine göre bir stil alır.

```csharp
public Style this[int index] { get; }
```

## Örnekler

Bir belgenin stil koleksiyonuna nasıl Stil ekleneceğini gösterir.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Daha sonra bu koleksiyona ekleyebileceğimiz yeni stiller için varsayılan parametreleri ayarlayın.
styles.DefaultFont.Name = "Courier New";
// "StyleType.Paragraph" stilini eklersek koleksiyon şu değerleri uygulayacaktır:
// "DefaultParagraphFormat" özelliğini stilin "ParagraphFormat" özelliğine dönüştürüyoruz.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Bir stil ekleyin ve ardından bunun varsayılan ayarlara sahip olduğunu doğrulayın.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Ayrıca bakınız

* class [Style](../../style/)
* class [StyleCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
