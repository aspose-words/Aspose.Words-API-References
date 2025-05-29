---
title: FileFormatInfo.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: .NET için Aspose.Words
description: Belge kodlamasını zahmetsizce tanımlamak için FileFormatInfo Encoding özelliğini keşfedin. Şu anda doğru sonuçlar için HTML formatlarını destekler.
type: docs
weight: 10
url: /tr/net/aspose.words/fileformatinfo/encoding/
---
## FileFormatInfo.Encoding property

Geçerli belge biçimine uygulanabilirse algılanan kodlamayı alır. Şu anda yalnızca HTML belgeleri için kodlamayı algılar.

```csharp
public Encoding Encoding { get; }
```

## Örnekler

Bir html dosyasındaki kodlamanın nasıl tespit edileceğini gösterir.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// Encoding özelliği yalnızca bir html belgesi için FileFormatInfo nesnesi oluşturduğumuzda kullanılır.
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### Ayrıca bakınız

* class [FileFormatInfo](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
