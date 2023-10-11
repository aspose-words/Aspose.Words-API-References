---
title: FileFormatInfo.Encoding
second_title: Aspose.Words for .NET API Referansı
description: FileFormatInfo mülk. Geçerli belge biçimine uygunsa algılanan kodlamayı alır. Şu anda yalnızca HTML belgeleri için kodlamayı algılar.
type: docs
weight: 10
url: /tr/net/aspose.words/fileformatinfo/encoding/
---
## FileFormatInfo.Encoding property

Geçerli belge biçimine uygunsa, algılanan kodlamayı alır. Şu anda yalnızca HTML belgeleri için kodlamayı algılar.

```csharp
public Encoding Encoding { get; }
```

### Örnekler

Bir html dosyasındaki kodlamanın nasıl algılanacağını gösterir.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// Encoding özelliği yalnızca bir html belgesi için FileFormatInfo nesnesi oluşturduğumuzda kullanılır.
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### Ayrıca bakınız

* class [FileFormatInfo](../)
* ad alanı [Aspose.Words](../../fileformatinfo/)
* toplantı [Aspose.Words](../../../)


