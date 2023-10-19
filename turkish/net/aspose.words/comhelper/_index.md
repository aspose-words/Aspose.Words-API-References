---
title: ComHelper Class
linktitle: ComHelper
articleTitle: ComHelper
second_title: Aspose.Words for .NET
description: Aspose.Words.ComHelper sınıf. COM istemcilerinin Aspose.Wordse belge yüklemesi için yöntemler sağlar C#'da.
type: docs
weight: 220
url: /tr/net/aspose.words/comhelper/
---
## ComHelper class

COM istemcilerinin Aspose.Words'e belge yüklemesi için yöntemler sağlar.

```csharp
public class ComHelper
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [ComHelper](comhelper/)() | Bu sınıfın yeni bir örneğini başlatır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Open](../../aspose.words/comhelper/open/#open)(*Stream*) | Bir COM uygulamasının yüklenmesine izin verir[`Document`](../document/) bir akıştan. |
| [Open](../../aspose.words/comhelper/open/#open_1)(*string*) | COM uygulamasının bir dosya yüklemesine izin verir.[`Document`](../document/) bir dosyadan. |
| [OpenIStream](../../aspose.words/comhelper/openistream/)(*IStream*) | COM uygulamasının bir dosya yüklemesine izin verir.[`Document`](../document/) bir IStream nesnesinden. |

## Notlar

Kullan`ComHelper` bir dosyadan veya akıştan bir belgeyi 'ye yüklemek için sınıf[`Document`](../document/) COM uygulamasındaki nesne.

[`Document`](../document/) sınıfı, yeni bir document oluşturmak için varsayılan bir kurucu sağlar ve ayrıca bir dosyadan veya akıştan belge yüklemek için aşırı yüklenmiş kurucular sağlar. Aspose.Words'ü bir .NET uygulamasından kullanıyorsanız, tüm[`Document`](../document/) yapıcılarını doğrudan kullanın, ancak Aspose.Words'ü bir COM uygulamasından kullanıyorsanız, yalnızca varsayılandır[`Document`](../document/) yapıcı mevcuttur.

## Örnekler

```csharp
[VBScript]

Dim helper
Set helper = CreateObject("Aspose.Words.ComHelper")

Dim doc
Set doc = helper.Open(fileName)
```

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
