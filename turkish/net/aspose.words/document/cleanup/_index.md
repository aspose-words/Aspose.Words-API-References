---
title: Document.Cleanup
linktitle: Cleanup
articleTitle: Cleanup
second_title: Aspose.Words for .NET
description: Document Cleanup yöntem. Belgedeki kullanılmayan stilleri ve listeleri temizler C#'da.
type: docs
weight: 540
url: /tr/net/aspose.words/document/cleanup/
---
## Cleanup() {#cleanup}

Belgedeki kullanılmayan stilleri ve listeleri temizler.

```csharp
public void Cleanup()
```

## Örnekler

Kullanılmayan özel stillerin bir belgeden nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// Yerleşik stillerle birleştirildiğinde belgenin artık sekiz stili var.
// Özel bir stil, belgenin bir kısmına uygulandığında "kullanılmış" olarak sayılır,
// bu, eklediğimiz dört stilin şu anda kullanılmadığı anlamına gelir.
Assert.AreEqual(8, doc.Styles.Count);

// Özel bir karakter stili ve ardından özel bir liste stili uygulayın. Bunu yapmak stilleri "kullanılmış" olarak işaretleyecektir.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

doc.Cleanup();

Assert.AreEqual(6, doc.Styles.Count);

// Özel bir stilin uygulandığı her düğümün kaldırılması, onu tekrar "kullanılmamış" olarak işaretler.
// Bunları kaldırmak için Temizleme yöntemini tekrar çalıştırın.
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup();

Assert.AreEqual(4, doc.Styles.Count);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Cleanup(*[CleanupOptions](../../cleanupoptions/)*) {#cleanup_1}

Verilenlere bağlı olarak kullanılmayan stilleri ve listeleri belgeden temizler.[`CleanupOptions`](../../cleanupoptions/) .

```csharp
public void Cleanup(CleanupOptions options)
```

## Örnekler

Kullanılmayan tüm özel stillerin bir belgeden nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// Yerleşik stillerle birleştirildiğinde belgenin artık sekiz stili var.
// Belgede herhangi bir metin varken özel stil "kullanılmış" olarak işaretlenir
// bu tarzda biçimlendirilmiş. Bu, eklediğimiz 4 stilin şu anda kullanılmadığı anlamına gelir.
Assert.AreEqual(8, doc.Styles.Count);

// Özel bir karakter stili ve ardından özel bir liste stili uygulayın. Bunu yaptığınızda bunlar "kullanılmış" olarak işaretlenir.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

// Artık kullanılmayan bir karakter stili ve kullanılmayan bir liste stili var.
// Cleanup() yöntemi, bir CleanupOptions nesnesiyle yapılandırıldığında kullanılmayan stilleri hedefleyebilir ve bunları kaldırabilir.
CleanupOptions cleanupOptions = new CleanupOptions
{
    UnusedLists = true, UnusedStyles = true, UnusedBuiltinStyles = true
};

doc.Cleanup(cleanupOptions);

Assert.AreEqual(4, doc.Styles.Count);

 // Özel bir stilin uygulandığı her düğümün kaldırılması, onu tekrar "kullanılmamış" olarak işaretler.
// Bunları kaldırmak için Temizleme yöntemini yeniden çalıştırın.
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup(cleanupOptions);

Assert.AreEqual(2, doc.Styles.Count);
```

### Ayrıca bakınız

* class [CleanupOptions](../../cleanupoptions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
