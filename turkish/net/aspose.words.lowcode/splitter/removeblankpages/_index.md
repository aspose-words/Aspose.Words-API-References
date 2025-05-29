---
title: Splitter.RemoveBlankPages
linktitle: RemoveBlankPages
articleTitle: RemoveBlankPages
second_title: .NET için Aspose.Words
description: Splitter RemoveBlankPages yöntemi ile belgelerinizden boş sayfaları zahmetsizce ortadan kaldırın. Zamandan tasarruf edin ve iş akışınızı bugün geliştirin!
type: docs
weight: 30
url: /tr/net/aspose.words.lowcode/splitter/removeblankpages/
---
## RemoveBlankPages(*string, string*) {#removeblankpages_2}

Belgeden boş sayfaları kaldırır ve çıktıyı kaydeder. Kaldırılan sayfa numaralarının bir listesini döndürür.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |

### Geri dönüş değeri

Sayfa numaraları listesi boş kabul edilerek kaldırılmıştır.

## Örnekler

Belgeden boş sayfaların nasıl kaldırılacağını gösterir.

```csharp
// Belgeden boş sayfaları kaldırmanın birkaç yolu vardır:
string doc = MyDir + "Blank pages.docx";

Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.1.docx");
Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.2.docx", SaveFormat.Docx);
```

### Ayrıca bakınız

* class [Splitter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## RemoveBlankPages(*string, string, [SaveFormat](../../../aspose.words/saveformat/)*) {#removeblankpages_3}

Belgeden boş sayfaları kaldırır ve çıktıyı belirtilen biçimde kaydeder. Kaldırılan sayfa numaralarının bir listesini döndürür.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName, 
    SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| saveFormat | SaveFormat | Kaydetme biçimi. |

### Geri dönüş değeri

Sayfa numaraları listesi boş kabul edilerek kaldırılmıştır.

## Örnekler

Belgeden boş sayfaların nasıl kaldırılacağını gösterir.

```csharp
// Belgeden boş sayfaları kaldırmanın birkaç yolu vardır:
string doc = MyDir + "Blank pages.docx";

Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.1.docx");
Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.2.docx", SaveFormat.Docx);
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## RemoveBlankPages(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#removeblankpages_4}

Belgeden boş sayfaları kaldırır ve çıktıyı belirtilen biçimde kaydeder. Kaldırılan sayfa numaralarının bir listesini döndürür.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName, 
    SaveOptions saveOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| saveOptions | SaveOptions | Kaydetme seçenekleri. |

### Geri dönüş değeri

Sayfa numaraları listesi boş kabul edilerek kaldırılmıştır.

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## RemoveBlankPages(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#removeblankpages}

Giriş akışında sağlanan bir belgeden boş sayfaları kaldırır ve güncellenen belgeyi belirtilen kaydetme biçiminde bir çıktı akışına kaydeder. Kaldırılan sayfa numaralarının bir listesini döndürür.

```csharp
public static List<int> RemoveBlankPages(Stream inputStream, Stream outputStream, 
    SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş akışı. |
| outputStream | Stream | Çıktı akışı. |
| saveFormat | SaveFormat | Kaydetme biçimi. |

### Geri dönüş değeri

Sayfa numaraları listesi boş kabul edilerek kaldırılmıştır.

## Örnekler

Akıştaki belgeden boş sayfaların nasıl kaldırılacağını gösterir.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Blank pages.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.RemoveBlankPagesStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Splitter.RemoveBlankPages(streamIn, streamOut, SaveFormat.Docx);
}
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## RemoveBlankPages(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#removeblankpages_1}

Giriş akışında sağlanan bir belgeden boş sayfaları kaldırır ve güncellenen belgeyi belirtilen kaydetme biçiminde bir çıktı akışına kaydeder. Kaldırılan sayfa numaralarının bir listesini döndürür.

```csharp
public static List<int> RemoveBlankPages(Stream inputStream, Stream outputStream, 
    SaveOptions saveOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş akışı. |
| outputStream | Stream | Çıktı akışı. |
| saveOptions | SaveOptions | Kaydetme seçenekleri. |

### Geri dönüş değeri

Sayfa numaraları listesi boş kabul edilerek kaldırılmıştır.

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)
