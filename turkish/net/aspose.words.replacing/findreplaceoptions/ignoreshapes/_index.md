---
title: FindReplaceOptions.IgnoreShapes
second_title: Aspose.Words for .NET API Referansı
description: FindReplaceOptions mülk. Bir metin içindeki şekillerin yoksayılacağını belirten bir boole değeri alır veya ayarlar.
type: docs
weight: 110
url: /tr/net/aspose.words.replacing/findreplaceoptions/ignoreshapes/
---
## FindReplaceOptions.IgnoreShapes property

Bir metin içindeki şekillerin yoksayılacağını belirten bir boole değeri alır veya ayarlar.

Varsayılan değer:`YANLIŞ`.

```csharp
public bool IgnoreShapes { get; set; }
```

### Örnekler

Metni değiştirirken şekillerin nasıl yok sayılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertShape(ShapeType.Balloon, 200, 200);            
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder.Document.Range.Replace("Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit.", new FindReplaceOptions() { IgnoreShapes = true });
Assert.AreEqual("Lorem ipsum dolor sit amet, consectetur adipiscing elit.", builder.Document.GetText().Trim());
```

### Ayrıca bakınız

* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../findreplaceoptions/)
* toplantı [Aspose.Words](../../../)


