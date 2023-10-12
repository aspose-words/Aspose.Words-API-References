---
title: ComHelper.ComHelper
second_title: Aspose.Words for .NET API Referansı
description: ComHelper inşaatçı. Bu sınıfın yeni bir örneğini başlatır.
type: docs
weight: 10
url: /tr/net/aspose.words/comhelper/comhelper/
---
## ComHelper constructor

Bu sınıfın yeni bir örneğini başlatır.

```csharp
public ComHelper()
```

### Örnekler

ComHelper sınıfını kullanarak belgelerin nasıl açılacağını gösterir.

```csharp
// ComHelper sınıfı, belgeleri COM istemcilerinden yüklememize olanak tanır.
ComHelper comHelper = new ComHelper();

// 1 - Yerel sistem dosya adını kullanma:
Document doc = comHelper.Open(MyDir + "Document.docx");

Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 2 - Bir akıştan:
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

### Ayrıca bakınız

* class [ComHelper](../)
* ad alanı [Aspose.Words](../../comhelper/)
* toplantı [Aspose.Words](../../../)


