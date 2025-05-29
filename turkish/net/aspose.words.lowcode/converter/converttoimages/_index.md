---
title: Converter.ConvertToImages
linktitle: ConvertToImages
articleTitle: ConvertToImages
second_title: .NET için Aspose.Words
description: ConvertToImages ile belgelerinizi zahmetsizce dönüştürün. Sayfaları gelişmiş paylaşım ve depolama için hızlı ve kolay bir şekilde yüksek kaliteli görüntü dosyalarına dönüştürün.
type: docs
weight: 30
url: /tr/net/aspose.words.lowcode/converter/converttoimages/
---
## ConvertToImages(*string, [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages_5}

Belirtilen giriş dosyasının sayfalarını belirtilen formattaki görüntülere dönüştürür ve görüntüleri içeren bir akış dizisi döndürür.

```csharp
public static Stream[] ConvertToImages(string inputFile, SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFile | String | Giriş dosya adı. |
| saveFormat | SaveFormat | Formatı kaydet. Sadece resim kaydetme formatlarına izin verilir. |

### Geri dönüş değeri

Görüntü akışlarının dizisini döndürür. Akışlar son kullanıcı tarafından atılmalıdır.

## Örnekler

Belgenin resim akışına nasıl dönüştürüleceğini gösterir.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ConvertToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_6}

Belirtilen giriş dosyasının sayfalarını belirtilen kaydetme seçeneklerini kullanarak görüntülere dönüştürür ve görüntüleri içeren bir akış dizisi döndürür.

```csharp
public static Stream[] ConvertToImages(string inputFile, ImageSaveOptions saveOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFile | String | Giriş dosya adı. |
| saveOptions | ImageSaveOptions | Resim kaydetme seçenekleri. |

### Geri dönüş değeri

Görüntü akışlarının dizisini döndürür. Akışlar son kullanıcı tarafından atılmalıdır.

## Örnekler

Belgenin resim akışına nasıl dönüştürüleceğini gösterir.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages_3}

Belirtilen giriş akışının sayfalarını belirtilen biçimdeki görüntülere dönüştürür ve görüntüleri içeren bir akış dizisi döndürür.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş akışı. |
| saveFormat | SaveFormat | Formatı kaydet. Sadece resim kaydetme formatlarına izin verilir. |

### Geri dönüş değeri

Görüntü akışlarının dizisini döndürür. Akışlar son kullanıcı tarafından atılmalıdır.

## Örnekler

Belgenin akıştan görüntüye nasıl dönüştürüleceğini gösterir.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);

    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = false };
    Converter.ConvertToImages(streamIn, loadOptions, imageSaveOptions);
}
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_4}

Belirtilen giriş akışının sayfalarını belirtilen kaydetme seçeneklerini kullanarak görüntülere dönüştürür ve görüntüleri içeren bir akış dizisi döndürür.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, ImageSaveOptions saveOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş akışı. |
| saveOptions | ImageSaveOptions | Resim kaydetme seçenekleri. |

### Geri dönüş değeri

Görüntü akışlarının dizisini döndürür. Akışlar son kullanıcı tarafından atılmalıdır.

## Örnekler

Belgenin akıştan görüntüye nasıl dönüştürüleceğini gösterir.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);

    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = false };
    Converter.ConvertToImages(streamIn, loadOptions, imageSaveOptions);
}
```

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/), [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_2}

Belirtilen giriş akışının sayfalarını, sağlanan yükleme ve kaydetme seçeneklerini kullanarak görüntülere dönüştürür ve görüntüleri içeren bir akış dizisi döndürür.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, LoadOptions loadOptions, 
    ImageSaveOptions saveOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş akışı. |
| loadOptions | LoadOptions | Giriş belgesi yükleme seçenekleri. |
| saveOptions | ImageSaveOptions | Resim kaydetme seçenekleri. |

### Geri dönüş değeri

Görüntü akışlarının dizisini döndürür. Akışlar son kullanıcı tarafından atılmalıdır.

## Örnekler

Belgenin akıştan görüntüye nasıl dönüştürüleceğini gösterir.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);

    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = false };
    Converter.ConvertToImages(streamIn, loadOptions, imageSaveOptions);
}
```

### Ayrıca bakınız

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ConvertToImages(*[Document](../../../aspose.words/document/), [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages}

Belirtilen belgenin sayfalarını belirtilen formattaki görüntülere dönüştürür ve görüntüleri içeren bir akış dizisi döndürür.

```csharp
public static Stream[] ConvertToImages(Document doc, SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | Document | Giriş belgesi. |
| saveFormat | SaveFormat | Formatı kaydet. Sadece resim kaydetme formatlarına izin verilir. |

### Geri dönüş değeri

Görüntü akışlarının dizisini döndürür. Akışlar son kullanıcı tarafından atılmalıdır.

## Örnekler

Belgenin resim akışına nasıl dönüştürüleceğini gösterir.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ConvertToImages(*[Document](../../../aspose.words/document/), [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_1}

Belirtilen belgenin sayfalarını belirtilen kaydetme seçeneklerini kullanarak görüntülere dönüştürür ve görüntüleri içeren bir akış dizisi döndürür.

```csharp
public static Stream[] ConvertToImages(Document doc, ImageSaveOptions saveOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | Document | Giriş belgesi. |
| saveOptions | ImageSaveOptions | Resim kaydetme seçenekleri. |

### Geri dönüş değeri

Görüntü akışlarının dizisini döndürür. Akışlar son kullanıcı tarafından atılmalıdır.

## Örnekler

Belgenin resim akışına nasıl dönüştürüleceğini gösterir.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)
