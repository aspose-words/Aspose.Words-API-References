---
title: ComHelper
linktitle: ComHelper
articleTitle: ComHelper
second_title: .NET için Aspose.Words
description: Programlama verimliliğinizi ve üretkenliğinizi artırarak yeni sınıf örneklerini zahmetsizce başlatan güçlü oluşturucu ComHelper'ı keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words/comhelper/comhelper/
---
## ComHelper constructor

Bu sınıfın yeni bir örneğini başlatır.

```csharp
public ComHelper()
```

## Örnekler

ComHelper sınıfını kullanarak belgelerin nasıl açılacağını gösterir.

```csharp
// ComHelper sınıfı, COM istemcilerinden belgeleri yüklememize olanak tanır.
ComHelper comHelper = new ComHelper();

// 1 - Yerel bir sistem dosya adı kullanarak:
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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
