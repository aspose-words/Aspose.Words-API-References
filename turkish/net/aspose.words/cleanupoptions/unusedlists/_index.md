---
title: CleanupOptions.UnusedLists
linktitle: UnusedLists
articleTitle: UnusedLists
second_title: .NET için Aspose.Words
description: CleanupOptions'ın UnusedLists özelliğiyle belgelerinizi optimize edin. Daha temiz, daha verimli bir çalışma alanı için kullanılmayan listeleri ve tanımları kolayca kaldırın.
type: docs
weight: 40
url: /tr/net/aspose.words/cleanupoptions/unusedlists/
---
## CleanupOptions.UnusedLists property

Kullanılmayan liste ve liste tanımlarının belgeden kaldırılıp kaldırılmayacağını belirtir. Varsayılan değer`doğru` .

```csharp
public bool UnusedLists { get; set; }
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

* class [CleanupOptions](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
