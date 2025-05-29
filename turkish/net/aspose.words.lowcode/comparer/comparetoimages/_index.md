---
title: Comparer.CompareToImages
linktitle: CompareToImages
articleTitle: CompareToImages
second_title: .NET için Aspose.Words
description: CompareToImages ile belgeleri zahmetsizce karşılaştırın, farkları her sayfa için resim olarak kaydedin, netliği ve görsel analizi geliştirin.
type: docs
weight: 30
url: /tr/net/aspose.words.lowcode/comparer/comparetoimages/
---
## CompareToImages(*string, string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#comparetoimages_1}

İki belgeyi karşılaştırır ve farkları resim olarak kaydeder. Döndürülen dizideki her öğe, çıktının resim olarak işlenen tek bir sayfasını temsil eder.

```csharp
public static Stream[] CompareToImages(string v1, string v2, ImageSaveOptions imageSaveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| v1 | String | Orijinal belge. |
| v2 | String | Değiştirilen belge. |
| imageSaveOptions | ImageSaveOptions | Çıktının görüntü kaydetme seçenekleri. |
| author | String | Revizyonlarda kullanılacak yazarın baş harfleri. |
| dateTime | DateTime | Revizyonlar için kullanılacak tarih ve saat. |
| compareOptions | CompareOptions | Belge karşılaştırma seçenekleri. |

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## CompareToImages(*Stream, Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#comparetoimages}

İki belgeyi karşılaştırır ve farkları resim olarak kaydeder. Döndürülen dizideki her öğe, çıktının resim olarak işlenen tek bir sayfasını temsil eder.

```csharp
public static Stream[] CompareToImages(Stream v1, Stream v2, ImageSaveOptions imageSaveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| v1 | Stream | Orijinal belge. |
| v2 | Stream | Değiştirilen belge. |
| imageSaveOptions | ImageSaveOptions | Çıktının görüntü kaydetme seçenekleri. |
| author | String | Revizyonlarda kullanılacak yazarın baş harfleri. |
| dateTime | DateTime | Revizyonlar için kullanılacak tarih ve saat. |
| compareOptions | CompareOptions | Belge karşılaştırma seçenekleri. |

## Örnekler

Belgelerin nasıl karşılaştırılacağını ve sonuçların resim olarak nasıl kaydedileceğini gösterir.

```csharp
// Belgeleri karşılaştırmanın birkaç yolu vardır:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Stream[] pages = Comparer.CompareToImages(firstDoc, secondDoc, new ImageSaveOptions(SaveFormat.Png), "Author", new DateTime());

using (FileStream firstStreamIn = new FileStream(firstDoc, FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(secondDoc, FileMode.Open, FileAccess.Read))
    {
        CompareOptions compareOptions = new CompareOptions();
        compareOptions.IgnoreCaseChanges = true;
        pages = Comparer.CompareToImages(firstStreamIn, secondStreamIn, new ImageSaveOptions(SaveFormat.Png), "Author", new DateTime(), compareOptions);
    }
}
```

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)
