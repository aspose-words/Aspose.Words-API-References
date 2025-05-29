---
title: Replacer.ReplaceToImages
linktitle: ReplaceToImages
articleTitle: ReplaceToImages
second_title: .NET için Aspose.Words
description: Karakter desenlerini özel dizelerle değiştirerek giriş dosyalarınızı zahmetsizce dönüştürün ve ReplaceToImages yöntemimizle çarpıcı görüntüler oluşturun.
type: docs
weight: 30
url: /tr/net/aspose.words.lowcode/replacer/replacetoimages/
---
## ReplaceToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_2}

Giriş dosyasında belirtilen karakter dizisi deseninin tüm oluşumlarını bir değiştirme dizesiyle değiştirir. Çıktıyı resimlere dönüştürür.

```csharp
public static Stream[] ReplaceToImages(string inputFileName, ImageSaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| saveOptions | ImageSaveOptions | Kaydetme seçenekleri. |
| pattern | String | Değiştirilmesi gereken bir dize. |
| replacement | String | Desenin tüm oluşumlarını değiştirecek bir dize. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) ek seçenekleri belirtmek için nesne. |

## Örnekler

Belgedeki dizenin nasıl değiştirileceğini ve sonucun resimlere nasıl kaydedileceğini gösterir.

```csharp
// Belgedeki dizeleri değiştirmenin birkaç yolu vardır:
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

Stream[] images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);

FindReplaceOptions options = new FindReplaceOptions();
options.FindWholeWordsOnly = false;
images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, options);
```

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ReplaceToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages}

Giriş dosyasında belirtilen karakter dizisi deseninin tüm oluşumlarını bir değiştirme dizesiyle değiştirir. Çıktıyı resimlere dönüştürür.

```csharp
public static Stream[] ReplaceToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş dosya akışı. |
| saveOptions | ImageSaveOptions | Kaydetme seçenekleri. |
| pattern | String | Değiştirilmesi gereken bir dize. |
| replacement | String | Desenin tüm oluşumlarını değiştirecek bir dize. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) ek seçenekleri belirtmek için nesne. |

## Örnekler

Belgedeki dizenin akıştaki belgeler kullanılarak nasıl değiştirileceğini ve sonucun resimlere nasıl kaydedileceğini gösterir.

```csharp
// Akıştaki belgeleri kullanarak belgedeki dizeyi değiştirmenin birkaç yolu vardır:
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

using (FileStream streamIn = new FileStream(MyDir + "Footer.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);

    FindReplaceOptions options = new FindReplaceOptions();
    options.FindWholeWordsOnly = false;
    images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, options);
}
```

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ReplaceToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_3}

Giriş dosyasında belirtilen düzenli ifade deseninin tüm oluşumlarını bir değiştirme dizesiyle değiştirir. Çıktıyı resimlere işler.

```csharp
public static Stream[] ReplaceToImages(string inputFileName, ImageSaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| saveOptions | ImageSaveOptions | Kaydetme seçenekleri. |
| pattern | Regex | Eşleşmeleri bulmak için kullanılan düzenli ifade deseni. |
| replacement | String | Desenin tüm oluşumlarını değiştirecek bir dize. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) ek seçenekleri belirtmek için nesne. |

## Örnekler

Belgedeki dizenin regex ile nasıl değiştirileceğini ve sonucun resimlere nasıl kaydedileceğini gösterir.

```csharp
// Belgede string ifadeleri regex ile değiştirmenin birkaç yolu vardır:
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

Stream[] images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);
images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
```

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ReplaceToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_1}

Giriş dosyasında belirtilen düzenli ifade deseninin tüm oluşumlarını bir değiştirme dizesiyle değiştirir. Çıktıyı resimlere işler.

```csharp
public static Stream[] ReplaceToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş dosya akışı. |
| saveOptions | ImageSaveOptions | Kaydetme seçenekleri. |
| pattern | Regex | Eşleşmeleri bulmak için kullanılan düzenli ifade deseni. |
| replacement | String | Desenin tüm oluşumlarını değiştirecek bir dize. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) ek seçenekleri belirtmek için nesne. |

## Örnekler

Akıştaki belgeleri kullanarak belgedeki dizenin regex ile nasıl değiştirileceğini ve sonucun resimlere nasıl kaydedileceğini gösterir.

```csharp
// Akıştaki belgeleri kullanarak belgedeki dizeyi regex ile değiştirmenin birkaç yolu vardır:
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

using (FileStream streamIn = new FileStream(MyDir + "Replace regex.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);
    images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
}
```

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)
