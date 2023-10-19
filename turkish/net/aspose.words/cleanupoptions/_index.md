---
title: CleanupOptions Class
linktitle: CleanupOptions
articleTitle: CleanupOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.CleanupOptions sınıf. Belge temizleme seçeneklerini belirlemeye izin verir C#'da.
type: docs
weight: 210
url: /tr/net/aspose.words/cleanupoptions/
---
## CleanupOptions class

Belge temizleme seçeneklerini belirlemeye izin verir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Belgeyi Temizleme](https://docs.aspose.com/words/net/clean-up-a-document/) dokümantasyon makalesi.

```csharp
public class CleanupOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [CleanupOptions](cleanupoptions/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DuplicateStyle](../../aspose.words/cleanupoptions/duplicatestyle/) { get; set; } | Yinelenen stillerin belgeden kaldırılması gerekip gerekmediğini belirten bir bayrak alır/ayarlar. Varsayılan değer:`YANLIŞ` . |
| [UnusedBuiltinStyles](../../aspose.words/cleanupoptions/unusedbuiltinstyles/) { get; set; } | Kullanılmadığını belirtir[`BuiltIn`](../style/builtin/) stiller belgeden kaldırılmalıdır. |
| [UnusedLists](../../aspose.words/cleanupoptions/unusedlists/) { get; set; } | Kullanılmayan liste ve liste tanımlarının belgeden kaldırılıp kaldırılmayacağını belirtir. Varsayılan değer:`doğru` . |
| [UnusedStyles](../../aspose.words/cleanupoptions/unusedstyles/) { get; set; } | Kullanılmayan stillerin belgeden kaldırılıp kaldırılmayacağını belirtir. Varsayılan değer:`doğru` . |

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
