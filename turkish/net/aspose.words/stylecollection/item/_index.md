---
title: StyleCollection.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: StyleCollection'ın güçlü Öğe özelliğini keşfedin ve stilleri adlarına veya takma adlarına göre zahmetsizce alın, tasarım deneyiminizi kolaylıkla geliştirin!
type: docs
weight: 50
url: /tr/net/aspose.words/stylecollection/item/
---
## StyleCollection indexer (1 of 3)

Adına veya takma adına göre bir stil alır.

```csharp
public Style this[string name] { get; }
```

## Notlar

Büyük/küçük harfe duyarlı, döner`hükümsüz` Belirtilen isimde stil bulunamazsa.

Eğer bu henüz var olmayan yerleşik bir stilin İngilizce adı ise, otomatik olarak oluşturur.

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

### Ayrıca bakınız

* class [Style](../../style/)
* class [StyleCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## StyleCollection indexer (2 of 3)

Yerel bağımsız tanımlayıcısı ile yerleşik bir stil alır.

```csharp
public Style this[StyleIdentifier sti] { get; }
```

| Parametre | Tanım |
| --- | --- |
| sti | A[`StyleIdentifier`](../../styleidentifier/) Alınacak yerleşik stili belirten değer. |

## Notlar

Henüz var olmayan bir stile erişildiğinde, otomatik olarak oluşturulur.

## Örnekler

Bir belgenin stiller koleksiyonuna Stil eklemenin nasıl yapılacağını gösterir.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Daha sonra bu koleksiyona ekleyebileceğimiz yeni stiller için varsayılan parametreleri ayarlayın.
styles.DefaultFont.Name = "Courier New";
// "StyleType.Paragraph" stilini eklersek, koleksiyon şu değerleri uygulayacaktır:
// "DefaultParagraphFormat" özelliğini stilin "ParagraphFormat" özelliğine.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Bir stil ekleyin ve ardından varsayılan ayarlara sahip olduğunu doğrulayın.
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

Dizinle bir stil alır.

```csharp
public Style this[int index] { get; }
```

## Örnekler

Bir belgenin stiller koleksiyonuna Stil eklemenin nasıl yapılacağını gösterir.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Daha sonra bu koleksiyona ekleyebileceğimiz yeni stiller için varsayılan parametreleri ayarlayın.
styles.DefaultFont.Name = "Courier New";
// "StyleType.Paragraph" stilini eklersek, koleksiyon şu değerleri uygulayacaktır:
// "DefaultParagraphFormat" özelliğini stilin "ParagraphFormat" özelliğine.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Bir stil ekleyin ve ardından varsayılan ayarlara sahip olduğunu doğrulayın.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Ayrıca bakınız

* class [Style](../../style/)
* class [StyleCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
