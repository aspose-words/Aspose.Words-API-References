---
title: Converter.Convert
linktitle: Convert
articleTitle: Convert
second_title: .NET için Aspose.Words
description: Belgelerinizi Dönüştürücümüzün Dönüştürme yöntemiyle zahmetsizce dönüştürün. Giriş dosyalarını kolaylıkla ve hassasiyetle istediğiniz formatlara dönüştürün.
type: docs
weight: 20
url: /tr/net/aspose.words.lowcode/converter/convert/
---
## Convert(*string, string*) {#convert_4}

Belirtilen giriş-çıkış dosya adlarını ve uzantılarını kullanarak verilen giriş belgesini çıkış belgesine dönüştürür.

```csharp
public static void Convert(string inputFile, string outputFile)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFile | String | Giriş dosya adı. |
| outputFile | String | Çıktı dosyasının adı. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Örnekler

Tek bir kod satırıyla belgelerin nasıl dönüştürüleceğini gösterir.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### Ayrıca bakınız

* class [Converter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Convert(*string, string, [SaveFormat](../../../aspose.words/saveformat/)*) {#convert_5}

Belirtilen giriş-çıkış dosya adlarını ve son belge biçimini kullanarak verilen giriş belgesini çıkış belgesine dönüştürür.

```csharp
public static void Convert(string inputFile, string outputFile, SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFile | String | Giriş dosya adı. |
| outputFile | String | Çıktı dosyasının adı. |
| saveFormat | SaveFormat | Kaydetme biçimi. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Örnekler

Tek bir kod satırıyla belgelerin nasıl dönüştürüleceğini gösterir.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Convert(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert_6}

Belirtilen giriş-çıkış dosya adlarını ve kaydetme seçeneklerini kullanarak belirtilen giriş belgesini çıkış belgesine dönüştürür.

```csharp
public static void Convert(string inputFile, string outputFile, SaveOptions saveOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFile | String | Giriş dosya adı. |
| outputFile | String | Çıktı dosyasının adı. |
| saveOptions | SaveOptions | Kaydetme seçenekleri. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Örnekler

Tek bir kod satırıyla belgelerin nasıl dönüştürüleceğini gösterir.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Convert(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/), string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert_3}

Belirtilen giriş çıktı dosya adlarını ve yükleme/kaydetme seçeneklerini kullanarak belirtilen giriş belgesini çıkış belgesine dönüştürür.

```csharp
public static void Convert(string inputFile, LoadOptions loadOptions, string outputFile, 
    SaveOptions saveOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFile | String | Giriş dosya adı. |
| loadOptions | LoadOptions | Giriş belgesi yükleme seçenekleri. |
| outputFile | String | Çıktı dosyasının adı. |
| saveOptions | SaveOptions | Kaydetme seçenekleri. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Örnekler

Tek bir kod satırıyla belgelerin nasıl dönüştürüleceğini gösterir.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### Ayrıca bakınız

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Convert(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#convert_1}

Belirtilen giriş ve çıkış akışlarını kullanarak verilen giriş belgesini tek bir çıkış belgesine dönüştürür.

```csharp
public static void Convert(Stream inputStream, Stream outputStream, SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş akışı. |
| outputStream | Stream | Çıktı akışı. |
| saveFormat | SaveFormat | Kaydetme biçimi. |

## Notlar

Çıkış biçimi bir resim ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), belirtilen akışa yalnızca çıkışın ilk sayfası kaydedilir.

Çıkış biçimi TIFF ise, çıkış belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Örnekler

Belgelerin tek bir satır kodla (Stream) nasıl dönüştürüleceğini gösterir.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, SaveFormat.Docx);

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, loadOptions, streamOut, saveOptions);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, saveOptions);
}
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Convert(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert_2}

Belirtilen giriş ve çıkış akışlarını kullanarak verilen giriş belgesini tek bir çıkış belgesine dönüştürür.

```csharp
public static void Convert(Stream inputStream, Stream outputStream, SaveOptions saveOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş akışları. |
| outputStream | Stream | Çıktı akışı. |
| saveOptions | SaveOptions | Kaydetme seçenekleri. |

## Notlar

Çıkış biçimi bir resim ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), belirtilen akışa yalnızca çıkışın ilk sayfası kaydedilir.

Çıkış biçimi TIFF ise, çıkış belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Örnekler

Belgelerin tek bir satır kodla (Stream) nasıl dönüştürüleceğini gösterir.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, SaveFormat.Docx);

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, loadOptions, streamOut, saveOptions);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, saveOptions);
}
```

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Convert(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/), Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert}

Belirtilen giriş ve çıkış akışlarını kullanarak verilen giriş belgesini tek bir çıkış belgesine dönüştürür.

```csharp
public static void Convert(Stream inputStream, LoadOptions loadOptions, Stream outputStream, 
    SaveOptions saveOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş akışları. |
| loadOptions | LoadOptions | Giriş belgesi yükleme seçenekleri. |
| outputStream | Stream | Çıktı akışı. |
| saveOptions | SaveOptions | Kaydetme seçenekleri. |

## Notlar

Çıkış biçimi bir resim ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), belirtilen akışa yalnızca çıkışın ilk sayfası kaydedilir.

Çıkış biçimi TIFF ise, çıkış belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Örnekler

Belgelerin tek bir satır kodla (Stream) nasıl dönüştürüleceğini gösterir.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, SaveFormat.Docx);

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, loadOptions, streamOut, saveOptions);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, saveOptions);
}
```

### Ayrıca bakınız

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)
