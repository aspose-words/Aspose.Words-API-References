---
title: "Aspose::Words::LowCode::Watermarker::SetText metodu"
linktitle: "SetText"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::LowCode::Watermarker::SetText metodu. C++'ta seçeneklerle akışlardan belgeye metin filigranı ekler."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.lowcode/watermarker/settext/
---
## Watermarker::SetText(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&) method


Belgeye akışlardan seçeneklerle bir metin filigranı ekler.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkText)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |
| watermarkText | const System::String\& | Filigran olarak görüntülenen metin. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Belgeye akışlardan seçeneklerle bir metin filigranı ekler.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |
| watermarkText | const System::String\& | Filigran olarak görüntülenen metin. |
| seçenekler | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Metin filigranı için ek seçenekleri tanımlar. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) method


Belgeye akışlardan seçeneklerle bir metin filigranı ekler.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkText)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
| watermarkText | const System::String\& | Filigran olarak görüntülenen metin. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Belgeye akışlardan seçeneklerle bir metin filigranı ekler.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
| watermarkText | const System::String\& | Filigran olarak görüntülenen metin. |
| seçenekler | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Metin filigranı için ek seçenekleri tanımlar. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) method


Belgeye seçenekler ve belirtilen kaydetme formatı ile bir metin filigranı ekler.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkText)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |
| watermarkText | const System::String\& | Filigran olarak görüntülenen metin. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Belgeye seçenekler ve belirtilen kaydetme formatı ile bir metin filigranı ekler.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |
| watermarkText | const System::String\& | Filigran olarak görüntülenen metin. |
| seçenekler | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Metin filigranı için ek seçenekleri tanımlar. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) method


Belgeye seçenekler ve belirtilen kaydetme formatı ile bir metin filigranı ekler.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkText)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
| watermarkText | const System::String\& | Filigran olarak görüntülenen metin. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Belgeye seçenekler ve belirtilen kaydetme formatı ile bir metin filigranı ekler.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
| watermarkText | const System::String\& | Filigran olarak görüntülenen metin. |
| seçenekler | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Metin filigranı için ek seçenekleri tanımlar. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, const System::String\&) method


Belgeye bir metin filigranı ekler.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkText)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| watermarkText | const System::String\& | Filigran olarak görüntülenen metin. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Belgeye seçeneklerle bir metin filigranı ekler.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| watermarkText | const System::String\& | Filigran olarak görüntülenen metin. |
| seçenekler | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Metin filigranı için ek seçenekleri tanımlar. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
