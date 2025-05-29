---
title: Range.Text
linktitle: Text
articleTitle: Text
second_title: .NET için Aspose.Words
description: Gelişmiş içerik yönetimi için belirtilen bir aralıktaki metni kolayca almak ve düzenlemek amacıyla Aralık Metni özelliğini keşfedin.
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

Döndürülen dize, aşağıda açıklandığı gibi tüm denetim ve özel karakterleri içerir[`ControlChar`](../../controlchar/).

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
