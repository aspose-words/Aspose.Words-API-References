---
title: FindReplaceOptions.IgnoreShapes
linktitle: IgnoreShapes
articleTitle: IgnoreShapes
second_title: .NET için Aspose.Words
description: FindReplaceOptions'ın IgnoreShapes özelliğini keşfedin. Bu temel boolean ayarıyla metin işlemede şekil eklemeyi kontrol ederek gelişmiş doğruluk elde edin.
type: docs
weight: 110
url: /tr/net/aspose.words.replacing/findreplaceoptions/ignoreshapes/
---
## FindReplaceOptions.IgnoreShapes property

Bir metin içindeki şekillerin göz ardı edileceğini belirten bir Boole değeri alır veya ayarlar.

Varsayılan değer:`YANLIŞ`.

```csharp
public bool IgnoreShapes { get; set; }
```

## Örnekler

Metni değiştirirken şekillerin nasıl göz ardı edileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertShape(ShapeType.Balloon, 200, 200);
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

FindReplaceOptions findReplaceOptions = new FindReplaceOptions() { IgnoreShapes = true };
builder.Document.Range.Replace("Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit.", findReplaceOptions);
Assert.AreEqual("Lorem ipsum dolor sit amet, consectetur adipiscing elit.", builder.Document.GetText().Trim());
```

### Ayrıca bakınız

* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)
