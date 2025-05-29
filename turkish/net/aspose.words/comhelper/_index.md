---
title: ComHelper Class
linktitle: ComHelper
articleTitle: ComHelper
second_title: .NET için Aspose.Words
description: Aspose.Words.ComHelper ile kusursuz belge entegrasyonunun kilidini açın. Güçlü özelliklerle COM istemcileri için belgeleri zahmetsizce yükleyin ve yönetin.
type: docs
weight: 410
url: /tr/net/aspose.words/comhelper/
---
## ComHelper class

COM istemcilerinin bir belgeyi Aspose.Words'e yüklemesi için yöntemler sağlar.

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
| [Open](../../aspose.words/comhelper/open/#open)(*Stream*) | Bir COM uygulamasının yüklenmesine izin verir[`Document`](../document/) bir dereden. |
| [Open](../../aspose.words/comhelper/open/#open_1)(*string*) | Bir COM uygulamasının bir[`Document`](../document/) bir dosyadan. |
| [OpenIStream](../../aspose.words/comhelper/openistream/)(*IStream*) | Bir COM uygulamasının bir[`Document`](../document/) bir IStream nesnesinden. |

## Notlar

Kullanın`ComHelper` bir belgeyi bir dosyadan veya akıştan 'ye yüklemek için sınıf[`Document`](../document/) COM uygulamasındaki nesne.

The[`Document`](../document/) sınıf, yeni bir document oluşturmak için varsayılan bir oluşturucu sağlar ve ayrıca bir dosyadan veya akıştan bir belge yüklemek için aşırı yüklenmiş oluşturucular sağlar. Bir .NET uygulamasından Aspose.Words kullanıyorsanız, tüm[`Document`](../document/) yapıcıları doğrudan, ancak bir COM uygulamasından Aspose.Words kullanıyorsanız, yalnızca varsayılan[`Document`](../document/) yapıcı mevcuttur.

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
