---
title: Watermarker.SetText
linktitle: SetText
articleTitle: SetText
second_title: .NET için Aspose.Words
description: Belgelerinizi Watermarker SetText yöntemimizle geliştirin. Gelişmiş markalaşma ve profesyonellik için kolayca özelleştirilebilir metin filigranları ekleyin.
type: docs
weight: 30
url: /tr/net/aspose.words.lowcode/watermarker/settext/
---
## SetText(*string, string, string*) {#settext_4}

Belgeye bir metin filigranı ekler.

```csharp
public static void SetText(string inputFileName, string outputFileName, string watermarkText)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| watermarkText | String | Filigran olarak görüntülenen metin. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Örnekler

Belgeye filigran metninin nasıl ekleneceğini gösterir.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.1.docx", watermarkText);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.2.docx", SaveFormat.Docx, watermarkText);
TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.3.docx", watermarkText, watermarkOptions);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.4.docx", SaveFormat.Docx, watermarkText, watermarkOptions);
```

### Ayrıca bakınız

* class [Watermarker](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## SetText(*string, string, string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_5}

Belgeye seçeneklerle bir metin filigranı ekler.

```csharp
public static void SetText(string inputFileName, string outputFileName, string watermarkText, 
    TextWatermarkOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| watermarkText | String | Filigran olarak görüntülenen metin. |
| options | TextWatermarkOptions | Metin filigranı için ek seçenekleri tanımlar. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Örnekler

Belgeye filigran metninin nasıl ekleneceğini gösterir.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.1.docx", watermarkText);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.2.docx", SaveFormat.Docx, watermarkText);
TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.3.docx", watermarkText, watermarkOptions);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.4.docx", SaveFormat.Docx, watermarkText, watermarkOptions);
```

### Ayrıca bakınız

* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## SetText(*string, string, [SaveFormat](../../../aspose.words/saveformat/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_2}

Belgeye seçenekler ve belirtilen kaydetme biçimiyle bir metin filigranı ekler.

```csharp
public static void SetText(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| saveFormat | SaveFormat | Kaydetme biçimi. |
| watermarkText | String | Filigran olarak görüntülenen metin. |
| options | TextWatermarkOptions | Metin filigranı için ek seçenekleri tanımlar. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Örnekler

Belgeye filigran metninin nasıl ekleneceğini gösterir.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.1.docx", watermarkText);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.2.docx", SaveFormat.Docx, watermarkText);
TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.3.docx", watermarkText, watermarkOptions);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.4.docx", SaveFormat.Docx, watermarkText, watermarkOptions);
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## SetText(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_3}

Belgeye seçenekler ve belirtilen kaydetme biçimiyle bir metin filigranı ekler.

```csharp
public static void SetText(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| saveOptions | SaveOptions | Kaydetme seçenekleri. |
| watermarkText | String | Filigran olarak görüntülenen metin. |
| options | TextWatermarkOptions | Metin filigranı için ek seçenekleri tanımlar. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## SetText(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext}

Akışlardan seçeneklerle belgeye bir metin filigranı ekler.

```csharp
public static void SetText(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş akışı. |
| outputStream | Stream | Çıktı akışı. |
| saveFormat | SaveFormat | Kaydetme biçimi. |
| watermarkText | String | Filigran olarak görüntülenen metin. |
| options | TextWatermarkOptions | Metin filigranı için ek seçenekleri tanımlar. |

## Notlar

Çıkış biçimi bir resim ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), belirtilen akışa yalnızca çıkışın ilk sayfası kaydedilir.

Çıkış biçimi TIFF ise, çıkış belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Örnekler

Akıştan belgeye filigran metninin nasıl ekleneceğini gösterir.

```csharp
string watermarkText = "This is a watermark";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkTextStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.SetText(streamIn, streamOut, SaveFormat.Docx, watermarkText);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkTextStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
    {
        TextWatermarkOptions options = new TextWatermarkOptions();
        options.Color = Color.Red;
        Watermarker.SetText(streamIn, streamOut, SaveFormat.Docx, watermarkText, options);
    }
}
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## SetText(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_1}

Akışlardan seçeneklerle belgeye bir metin filigranı ekler.

```csharp
public static void SetText(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş akışı. |
| outputStream | Stream | Çıktı akışı. |
| saveOptions | SaveOptions | Kaydetme seçenekleri. |
| watermarkText | String | Filigran olarak görüntülenen metin. |
| options | TextWatermarkOptions | Metin filigranı için ek seçenekleri tanımlar. |

## Notlar

Çıkış biçimi bir resim ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), belirtilen akışa yalnızca çıkışın ilk sayfası kaydedilir.

Çıkış biçimi TIFF ise, çıkış belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)
