---
title: "Aspose::Words::LowCode::Watermarker::SetImage metodu"
linktitle: "SetImage"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::LowCode::Watermarker::SetImage metodu. C++'ta seçeneklerle akışlardan belgeye görüntü filigranı ekler."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.lowcode/watermarker/setimage/
---
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&) method


Belgeye akışlardan seçeneklerle bir görüntü filigranı ekler.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Drawing::Image> &watermarkImage)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Filigran olarak görüntülenen resim. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Belgeye akışlardan seçeneklerle bir görüntü filigranı ekler.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Drawing::Image> &watermarkImage, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Filigran olarak görüntülenen resim. |
| seçenekler | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Görüntü filigranı için ek seçenekleri tanımlar. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&) method


Belgeye akışlardan seçeneklerle bir görüntü filigranı ekler.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::IO::Stream> &watermarkImageStream)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Filigran olarak görüntülenen görüntü akışı. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Belgeye akışlardan seçeneklerle bir görüntü filigranı ekler.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::IO::Stream> &watermarkImageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Filigran olarak görüntülenen görüntü akışı. |
| seçenekler | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Görüntü filigranı için ek seçenekleri tanımlar. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&) method


Belgeye akışlardan seçeneklerle bir görüntü filigranı ekler.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Drawing::Image> &watermarkImage)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Filigran olarak görüntülenen resim. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Belgeye akışlardan seçeneklerle bir görüntü filigranı ekler.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Drawing::Image> &watermarkImage, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Filigran olarak görüntülenen resim. |
| seçenekler | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Görüntü filigranı için ek seçenekleri tanımlar. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Belgeye akışlardan seçeneklerle bir görüntü filigranı ekler.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::IO::Stream> &watermarkImageStream)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Filigran olarak görüntülenen görüntü akışı. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Belgeye akışlardan seçeneklerle bir görüntü filigranı ekler.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::IO::Stream> &watermarkImageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Filigran olarak görüntülenen görüntü akışı. |
| seçenekler | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Görüntü filigranı için ek seçenekleri tanımlar. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) method


Belgeye seçenekler ve belirtilen kaydetme formatı ile bir görüntü filigranı ekler.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkImageFileName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |
| watermarkImageFileName | const System::String\& | Filigran olarak görüntülenen resim. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Belgeye seçenekler ve belirtilen kaydetme formatı ile bir görüntü filigranı ekler.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |
| watermarkImageFileName | const System::String\& | Filigran olarak görüntülenen resim. |
| seçenekler | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Görüntü filigranı için ek seçenekleri tanımlar. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) method


Belgeye seçenekler ve belirtilen kaydetme formatı ile bir görüntü filigranı ekler.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkImageFileName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
| watermarkImageFileName | const System::String\& | Filigran olarak görüntülenen resim. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Belgeye seçenekler ve belirtilen kaydetme formatı ile bir görüntü filigranı ekler.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
| watermarkImageFileName | const System::String\& | Filigran olarak görüntülenen resim. |
| seçenekler | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Görüntü filigranı için ek seçenekleri tanımlar. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::String\&) method


Belgeye bir görüntü filigranı ekler.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkImageFileName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| watermarkImageFileName | const System::String\& | Filigran olarak görüntülenen resim. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Belgeye seçeneklerle bir görüntü filigranı ekler.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| watermarkImageFileName | const System::String\& | Filigran olarak görüntülenen resim. |
| seçenekler | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Görüntü filigranı için ek seçenekleri tanımlar. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
