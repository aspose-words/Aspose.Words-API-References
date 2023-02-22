---
title: Class ComHelper
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.ComHelper sınıf. COM istemcilerinin bir belgeyi Aspose.Wordse yüklemeleri için yöntemler sağlar.
type: docs
weight: 210
url: /tr/net/aspose.words/comhelper/
---
## ComHelper class

COM istemcilerinin bir belgeyi Aspose.Words'e yüklemeleri için yöntemler sağlar.

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
| [Open](../../aspose.words/comhelper/open/#open)(Stream) | Bir COM uygulamasının yüklenmesine izin verir[`Document`](../document/) bir akıştan. |
| [Open](../../aspose.words/comhelper/open/#open_1)(string) | Bir COM uygulamasının bir[`Document`](../document/) bir dosyadan. |
| [OpenIStream](../../aspose.words/comhelper/openistream/)(IStream) | Bir COM uygulamasının bir[`Document`](../document/) bir IStream nesnesinden. |

### Notlar

Kullan`ComHelper` bir dosyadan belge yüklemek veya bir dosyasına akış yapmak için sınıf[`Document`](../document/) COM uygulamasında nesne.

bu[`Document`](../document/)class, yeni bir document oluşturmak için varsayılan bir kurucu sağlar ve ayrıca bir dosyadan veya akıştan bir belge yüklemek için aşırı yüklenmiş kurucular sağlar. Bir .NET uygulamasından Aspose.Words kullanıyorsanız, tüm özellikleri kullanabilirsiniz.[`Document`](../document/) doğrudan yapılandırıcılar, ancak bir COM uygulamasından Aspose.Words kullanıyorsanız, yalnızca varsayılan[`Document`](../document/) yapıcı mevcuttur.

### Örnekler

```csharp
[VBScript]

Dim helper
Set helper = CreateObject("Aspose.Words.ComHelper")

Dim doc
Set doc = helper.Open(fileName)
```

ComHelper sınıfını kullanarak belgelerin nasıl açılacağını gösterir.

```csharp
// ComHelper sınıfı, COM istemcilerinden belgeleri yüklememize izin verir.
ComHelper comHelper = new ComHelper();

// 1 - Yerel bir sistem dosya adı kullanma:
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


