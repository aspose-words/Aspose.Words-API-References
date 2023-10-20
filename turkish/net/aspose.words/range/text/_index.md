---
title: Range.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: Range Text mülk. Aralığın metnini alır C#'da.
type: docs
weight: 60
url: /tr/net/aspose.words/range/text/
---
## Range.Text property

Aralığın metnini alır.

```csharp
public string Text { get; }
```

## Notlar

Döndürülen dize, yukarıda açıklandığı gibi tüm kontrol ve özel karakterleri içerir.[`ControlChar`](../../controlchar/).

## Örnekler

Bir aralığın kapsadığı tüm düğümlerin metin içeriklerinin nasıl alınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### Ayrıca bakınız

* class [Range](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
