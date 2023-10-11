---
title: CleanupOptions.DuplicateStyle
second_title: Aspose.Words for .NET API Referansı
description: CleanupOptions mülk. Yinelenen stillerin belgeden kaldırılması gerekip gerekmediğini belirten bir bayrak alır/ayarlar. Varsayılan değerYANLIŞ .
type: docs
weight: 20
url: /tr/net/aspose.words/cleanupoptions/duplicatestyle/
---
## CleanupOptions.DuplicateStyle property

Yinelenen stillerin belgeden kaldırılması gerekip gerekmediğini belirten bir bayrak alır/ayarlar. Varsayılan değer:`YANLIŞ` .

```csharp
public bool DuplicateStyle { get; set; }
```

### Örnekler

Yinelenen stillerin belgeden nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();

// Belgeye aynı özelliklere sahip iki stil ekleyin,
// ama farklı isimler. İkinci stil, birincinin kopyası olarak kabul edilir.
Style myStyle = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

Style duplicateStyle = doc.Styles.Add(StyleType.Paragraph, "MyStyle2");
duplicateStyle.Font.Size = 14;
duplicateStyle.Font.Name = "Courier New";
duplicateStyle.Font.Color = Color.Blue;

Assert.AreEqual(6, doc.Styles.Count);

// Her iki stili de belgedeki farklı paragraflara uygulayın.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

builder.ParagraphFormat.StyleName = duplicateStyle.Name;
builder.Writeln("Hello again!");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(myStyle, paragraphs[0].ParagraphFormat.Style);
Assert.AreEqual(duplicateStyle, paragraphs[1].ParagraphFormat.Style);

// Bir CleanOptions nesnesi yapılandırın, ardından tüm yinelenen stilleri değiştirmek için Cleanup yöntemini çağırın
// orijinali kullanın ve kopyaları belgeden kaldırın.
CleanupOptions cleanupOptions = new CleanupOptions { DuplicateStyle = true };

doc.Cleanup(cleanupOptions);

Assert.AreEqual(5, doc.Styles.Count);
Assert.AreEqual(myStyle, paragraphs[0].ParagraphFormat.Style);
Assert.AreEqual(myStyle, paragraphs[1].ParagraphFormat.Style);
```

### Ayrıca bakınız

* class [CleanupOptions](../)
* ad alanı [Aspose.Words](../../cleanupoptions/)
* toplantı [Aspose.Words](../../../)


