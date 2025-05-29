---
title: Splitter.ExtractPages
linktitle: ExtractPages
articleTitle: ExtractPages
second_title: .NET için Aspose.Words
description: Splitter ExtractPages yöntemimizle herhangi bir belgeden belirli sayfaları zahmetsizce çıkarın. Kolay erişim için istediğiniz biçimde kaydedin!
type: docs
weight: 20
url: /tr/net/aspose.words.lowcode/splitter/extractpages/
---
## ExtractPages(*string, string, int, int*) {#extractpages_4}

Bir belge dosyasından belirtilen bir sayfa aralığını ayıklar ve ayıklanan sayfaları yeni bir dosyaya kaydeder. Çıktı dosya biçimi, çıktı dosya adının uzantısı tarafından belirlenir.

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, int startPageIndex, 
    int pageCount)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| startPageIndex | Int32 | Çıkarılacak ilk sayfanın sıfır tabanlı indeksi. |
| pageCount | Int32 | Çıkarılacak sayfa sayısı. |

## Örnekler

Belgeden sayfaların nasıl çıkarılacağını gösterir.

```csharp
// Belgeden sayfaları çıkarmanın birkaç yolu vardır:
string doc = MyDir + "Big document.docx";

Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.1.docx", 0, 2);
Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.2.docx", SaveFormat.Docx, 0, 2);
```

### Ayrıca bakınız

* class [Splitter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ExtractPages(*string, string, [SaveFormat](../../../aspose.words/saveformat/), int, int*) {#extractpages_2}

Bir belge dosyasından belirtilen sayfa aralığını ayıklar ve ayıklanan sayfaları belirtilen kaydetme biçimini kullanarak yeni bir dosyaya kaydeder.

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    int startPageIndex, int pageCount)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| saveFormat | SaveFormat | Kaydetme biçimi. |
| startPageIndex | Int32 | Çıkarılacak ilk sayfanın sıfır tabanlı indeksi. |
| pageCount | Int32 | Çıkarılacak sayfa sayısı. |

## Örnekler

Belgeden sayfaların nasıl çıkarılacağını gösterir.

```csharp
// Belgeden sayfaları çıkarmanın birkaç yolu vardır:
string doc = MyDir + "Big document.docx";

Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.1.docx", 0, 2);
Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.2.docx", SaveFormat.Docx, 0, 2);
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ExtractPages(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), int, int*) {#extractpages_3}

Bir belge dosyasından belirtilen sayfa aralığını ayıklar ve ayıklanan sayfaları belirtilen kaydetme biçimini kullanarak yeni bir dosyaya kaydeder.

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, int startPageIndex, int pageCount)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| saveOptions | SaveOptions | Kaydetme seçenekleri. |
| startPageIndex | Int32 | Çıkarılacak ilk sayfanın sıfır tabanlı indeksi. |
| pageCount | Int32 | Çıkarılacak sayfa sayısı. |

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ExtractPages(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), int, int*) {#extractpages}

Bir belge akışından belirtilen sayfa aralığını ayıklar ve ayıklanan sayfaları belirtilen kaydetme biçimini kullanarak bir çıktı akışına kaydeder.

```csharp
public static void ExtractPages(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    int startPageIndex, int pageCount)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş akışı. |
| outputStream | Stream | Çıktı akışı. |
| saveFormat | SaveFormat | Kaydetme biçimi. |
| startPageIndex | Int32 | Çıkarılacak ilk sayfanın sıfır tabanlı indeksi. |
| pageCount | Int32 | Çıkarılacak sayfa sayısı. |

## Örnekler

Akıştan belgedeki sayfaların nasıl çıkarılacağını gösterir.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ExtractPagesStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Splitter.ExtractPages(streamIn, streamOut, SaveFormat.Docx, 0, 2);
}
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ExtractPages(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), int, int*) {#extractpages_1}

Bir belge akışından belirtilen sayfa aralığını ayıklar ve ayıklanan sayfaları belirtilen kaydetme biçimini kullanarak bir çıktı akışına kaydeder.

```csharp
public static void ExtractPages(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    int startPageIndex, int pageCount)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş akışı. |
| outputStream | Stream | Çıktı akışı. |
| saveOptions | SaveOptions | Kaydetme seçenekleri. |
| startPageIndex | Int32 | Çıkarılacak ilk sayfanın sıfır tabanlı indeksi. |
| pageCount | Int32 | Çıkarılacak sayfa sayısı. |

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)
