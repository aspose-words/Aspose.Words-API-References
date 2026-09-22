---
title: "Aspose::Words::LowCode::Converter::Convert yöntemi"
linktitle: "Dönüştür"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::LowCode::Converter::Convert yöntemi. Belirtilen giriş ve çıkış akışlarını kullanarak verilen giriş belgesini tek bir çıkış belgesine dönüştürür C++'da."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.lowcode/converter/convert/
---
## Converter::Convert(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Belirtilen giriş ve çıkış akışlarını kullanarak verilen giriş belgesini tek bir çıktı belgesine dönüştürür.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışları. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Giriş belgesi yükleme seçenekleri. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


Belirtilen giriş ve çıkış akışlarını kullanarak verilen giriş belgesini tek bir çıktı belgesine dönüştürür.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Belirtilen giriş ve çıkış akışlarını kullanarak verilen giriş belgesini tek bir çıktı belgesine dönüştürür.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışları. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Belirtilen giriş ve çıkış dosya adlarını ve yükleme/kaydetme seçeneklerini kullanarak verilen giriş belgesini çıktı belgesine dönüştürür.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFile | const System::String\& | Girdi dosya adı. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Giriş belgesi yükleme seçenekleri. |
| outputFile | const System::String\& | Çıktı dosya adı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::String\&) method


Belirtilen giriş ve çıkış dosya adlarını ve uzantılarını kullanarak verilen giriş belgesini çıkış belgesine dönüştürür.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::String &outputFile)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFile | const System::String\& | Girdi dosya adı. |
| outputFile | const System::String\& | Çıktı dosya adı. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) method


Belirtilen giriş ve çıkış dosya adlarını ve son belge formatını kullanarak verilen giriş belgesini çıktı belgesine dönüştürür.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::String &outputFile, Aspose::Words::SaveFormat saveFormat)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFile | const System::String\& | Girdi dosya adı. |
| outputFile | const System::String\& | Çıktı dosya adı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Belirtilen giriş ve çıkış dosya adlarını ve kaydetme seçeneklerini kullanarak verilen giriş belgesini çıktı belgesine dönüştürür.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFile | const System::String\& | Girdi dosya adı. |
| outputFile | const System::String\& | Çıktı dosya adı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
