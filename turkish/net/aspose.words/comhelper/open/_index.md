---
title: ComHelper.Open
linktitle: Open
articleTitle: Open
second_title: .NET için Aspose.Words
description: ComHelper'ın Open yöntemi ile kusursuz entegrasyonun kilidini açın ve COM uygulamalarınız için dosyalardan zahmetsiz belge yüklemeyi etkinleştirin.
type: docs
weight: 20
url: /tr/net/aspose.words/comhelper/open/
---
## Open(*string*) {#open_1}

Bir COM uygulamasının bir[`Document`](../../document/) bir dosyadan.

```csharp
public Document Open(string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Yüklenecek belgenin dosya adı. |

### Geri dönüş değeri

A[`Document`](../../document/) Word belgesini temsil eden nesne.

## Notlar

Bu yöntem, çağrı ile aynıdır[`Document`](../../document/) dosya adı parametresi olan yapıcı.

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

* class [Document](../../document/)
* class [ComHelper](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Open(*Stream*) {#open}

Bir COM uygulamasının yüklenmesine izin verir[`Document`](../../document/) bir dereden.

```csharp
public Document Open(Stream stream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Yüklenecek belgeyi içeren bir .NET akış nesnesi. |

### Geri dönüş değeri

A[`Document`](../../document/) Word belgesini temsil eden nesne.

## Notlar

Bu yöntem, çağrı ile aynıdır[`Document`](../../document/) akış parametresi olan bir kurucu.

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

* class [Document](../../document/)
* class [ComHelper](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
