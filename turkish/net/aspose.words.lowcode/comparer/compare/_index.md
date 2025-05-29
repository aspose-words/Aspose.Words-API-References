---
title: Comparer.Compare
linktitle: Compare
articleTitle: Compare
second_title: .NET için Aspose.Words
description: Karşılaştırma yöntemimizle iki belgeyi zahmetsizce karşılaştırın. Farklılıkları kaydedin ve düzenlemeleri ve biçim revizyonlarını tek bir çıktı dosyasında izleyin.
type: docs
weight: 20
url: /tr/net/aspose.words.lowcode/comparer/compare/
---
## Compare(*string, string, string, string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_4}

İki belgeyi ek seçeneklerle karşılaştırır ve farklılıkları belirtilen çıktı dosyasına kaydeder, değişiklikleri bir dizi düzenleme ve biçim revizyonu olarak üretir.

```csharp
public static void Compare(string v1, string v2, string outputFileName, string author, 
    DateTime dateTime, CompareOptions compareOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| v1 | String | Orijinal belge. |
| v2 | String | Değiştirilen belge. |
| outputFileName | String | Çıktı dosyasının adı. |
| author | String | Revizyonlarda kullanılacak yazarın baş harfleri. |
| dateTime | DateTime | Revizyonlar için kullanılacak tarih ve saat. |
| compareOptions | CompareOptions | Belge karşılaştırma seçenekleri. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Örnekler

Belgelerin nasıl basit bir şekilde karşılaştırılacağını gösterir.

```csharp
// Belgeleri karşılaştırmanın birkaç yolu vardır:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.1.docx", "Author", new DateTime());
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.2.docx", SaveFormat.Docx, "Author", new DateTime());

CompareOptions compareOptions = new CompareOptions();
compareOptions.IgnoreCaseChanges = true;
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.3.docx", "Author", new DateTime(), compareOptions);
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.4.docx", SaveFormat.Docx, "Author", new DateTime(), compareOptions);
```

### Ayrıca bakınız

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Compare(*string, string, string, [SaveFormat](../../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_2}

İki belgeyi ek seçeneklerle karşılaştırır ve farklılıkları belirtilen çıktı dosyasına sağlanan kaydetme biçiminde kaydeder, değişiklikleri bir dizi düzenleme ve biçim revizyonu olarak üretir.

```csharp
public static void Compare(string v1, string v2, string outputFileName, SaveFormat saveFormat, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| v1 | String | Orijinal belge. |
| v2 | String | Değiştirilen belge. |
| outputFileName | String | Çıktı dosyasının adı. |
| saveFormat | SaveFormat | Çıktının kaydedileceği format. |
| author | String | Revizyonlarda kullanılacak yazarın baş harfleri. |
| dateTime | DateTime | Revizyonlar için kullanılacak tarih ve saat. |
| compareOptions | CompareOptions | Belge karşılaştırma seçenekleri. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Örnekler

Belgelerin nasıl basit bir şekilde karşılaştırılacağını gösterir.

```csharp
// Belgeleri karşılaştırmanın birkaç yolu vardır:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.1.docx", "Author", new DateTime());
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.2.docx", SaveFormat.Docx, "Author", new DateTime());

CompareOptions compareOptions = new CompareOptions();
compareOptions.IgnoreCaseChanges = true;
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.3.docx", "Author", new DateTime(), compareOptions);
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.4.docx", SaveFormat.Docx, "Author", new DateTime(), compareOptions);
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Compare(*string, string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_3}

İki belgeyi ek seçeneklerle karşılaştırır ve farklılıkları belirtilen çıktı dosyasına sağlanan kaydetme biçiminde kaydeder, değişiklikleri bir dizi düzenleme ve biçim revizyonu olarak üretir.

```csharp
public static void Compare(string v1, string v2, string outputFileName, SaveOptions saveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| v1 | String | Orijinal belge. |
| v2 | String | Değiştirilen belge. |
| outputFileName | String | Çıktı dosyasının adı. |
| saveOptions | SaveOptions | Çıktının kaydetme seçenekleri. |
| author | String | Revizyonlarda kullanılacak yazarın baş harfleri. |
| dateTime | DateTime | Revizyonlar için kullanılacak tarih ve saat. |
| compareOptions | CompareOptions | Belge karşılaştırma seçenekleri. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Compare(*Stream, Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare}

Akışlardan yüklenen iki belgeyi ek seçeneklerle karşılaştırır ve farklılıkları belirtilen kaydetme biçiminde sağlanan çıktı akışına kaydeder, değişiklikleri bir dizi düzenleme ve biçim revizyonu olarak üretir.

```csharp
public static void Compare(Stream v1, Stream v2, Stream outputStream, SaveFormat saveFormat, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| v1 | Stream | Orijinal belge. |
| v2 | Stream | Değiştirilen belge. |
| outputStream | Stream | Çıktı akışı. |
| saveFormat | SaveFormat | Çıktının kaydedileceği format. |
| author | String | Revizyonlarda kullanılacak yazarın baş harfleri. |
| dateTime | DateTime | Revizyonlar için kullanılacak tarih ve saat. |
| compareOptions | CompareOptions | Belge karşılaştırma seçenekleri. |

## Notlar

Çıkış biçimi bir resim ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), belirtilen akışa yalnızca çıkışın ilk sayfası kaydedilir.

Çıkış biçimi TIFF ise, çıkış belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Örnekler

Akıştaki belgelerin nasıl karşılaştırılacağını gösterir.

```csharp
// Akıştaki belgeleri karşılaştırmanın birkaç yolu vardır:
using (FileStream firstStreamIn = new FileStream(MyDir + "Table column bookmarks.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Table column bookmarks.doc", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareStreamDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Comparer.Compare(firstStreamIn, secondStreamIn, streamOut, SaveFormat.Docx, "Author", new DateTime());

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareStreamDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
        {
            CompareOptions compareOptions = new CompareOptions();
            compareOptions.IgnoreCaseChanges = true;
            Comparer.Compare(firstStreamIn, secondStreamIn, streamOut, SaveFormat.Docx, "Author", new DateTime(), compareOptions);
        }
    }
}
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Compare(*Stream, Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_1}

Akışlardan yüklenen iki belgeyi ek seçeneklerle karşılaştırır ve farklılıkları belirtilen kaydetme biçiminde sağlanan çıktı akışına kaydeder, değişiklikleri bir dizi düzenleme ve biçim revizyonu olarak üretir.

```csharp
public static void Compare(Stream v1, Stream v2, Stream outputStream, SaveOptions saveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| v1 | Stream | Orijinal belge. |
| v2 | Stream | Değiştirilen belge. |
| outputStream | Stream | Çıktı akışı. |
| saveOptions | SaveOptions | Çıktının kaydetme seçenekleri. |
| author | String | Revizyonlarda kullanılacak yazarın baş harfleri. |
| dateTime | DateTime | Revizyonlar için kullanılacak tarih ve saat. |
| compareOptions | CompareOptions | Belge karşılaştırma seçenekleri. |

## Notlar

Çıkış biçimi bir resim ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), belirtilen akışa yalnızca çıkışın ilk sayfası kaydedilir.

Çıkış biçimi TIFF ise, çıkış belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)
