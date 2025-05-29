---
title: Document.Cleanup
linktitle: Cleanup
articleTitle: Cleanup
second_title: .NET için Aspose.Words
description: Belgelerinizi Temizleme yöntemimizle optimize edin; daha temiz, daha verimli bir iş akışı için kullanılmayan stilleri ve listeleri kaldırın. Bugün okunabilirliği artırın!
type: docs
weight: 580
url: /tr/net/aspose.words/document/cleanup/
---
## Cleanup() {#cleanup}

Belgeden kullanılmayan stilleri ve listeleri temizler.

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

// Yerleşik stillerle birlikte, belge artık sekiz stile sahip.
// Özel bir stil, belgenin bir bölümüne uygulandığında "kullanılmış" olarak sayılır.
// Bu, eklediğimiz dört stilin şu anda kullanılmadığı anlamına geliyor.
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

// Özel bir stilin uygulandığı her düğümün kaldırılması, onu tekrar "kullanılmayan" olarak işaretler.
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

Belirtilenlere bağlı olarak kullanılmayan stilleri ve listeleri belgeden temizler[`CleanupOptions`](../../cleanupoptions/) .

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

// Yerleşik stillerle birlikte, belge artık sekiz stile sahip.
// Belge içerisinde herhangi bir metin varken özel bir stil "kullanılmış" olarak işaretlenir
// o stilde biçimlendirildi. Bu, eklediğimiz 4 stilin şu anda kullanılmadığı anlamına geliyor.
Assert.AreEqual(8, doc.Styles.Count);

// Özel bir karakter stili ve ardından özel bir liste stili uygulayın. Bunu yapmak onları "kullanılmış" olarak işaretleyecektir.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

// Şimdi, kullanılmayan bir karakter stili ve kullanılmayan bir liste stili var.
// Cleanup() yöntemi, CleanupOptions nesnesiyle yapılandırıldığında kullanılmayan stilleri hedefleyebilir ve bunları kaldırabilir.
CleanupOptions cleanupOptions = new CleanupOptions
{
    UnusedLists = true, UnusedStyles = true, UnusedBuiltinStyles = true
};

doc.Cleanup(cleanupOptions);

Assert.AreEqual(4, doc.Styles.Count);

 // Özel bir stilin uygulandığı her düğümün kaldırılması, onu tekrar "kullanılmayan" olarak işaretler.
// Bunları kaldırmak için Temizleme yöntemini tekrar çalıştırın.
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup(cleanupOptions);

Assert.AreEqual(2, doc.Styles.Count);
```

### Ayrıca bakınız

* class [CleanupOptions](../../cleanupoptions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
