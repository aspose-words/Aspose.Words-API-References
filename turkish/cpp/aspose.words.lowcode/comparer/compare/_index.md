---
title: "Aspose::Words::LowCode::Comparer::Compare metodu"
linktitle: "Compare"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::LowCode::Comparer::Compare metodu. İki belgeyi akışlardan ek seçeneklerle yükler ve farkları belirtilen kaydetme biçiminde sağlanan çıktı akışına kaydeder, C++'ta bir dizi düzenleme ve biçim revizyonu olarak değişiklikler üretir."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.lowcode/comparer/compare/
---
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) method


Akışlardan yüklenen iki belgeyi ek seçeneklerle karşılaştırır ve farkları belirtilen kaydetme formatında sağlanan çıkış akışına kaydeder, değişiklikleri bir dizi düzenleme ve format revizyonu olarak üretir.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Orijinal belge. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Değiştirilmiş belge. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveFormat | Aspose::Words::SaveFormat | Çıktının kaydetme biçimi. |
| yazar | const System::String\& | Revizyonlar için kullanılacak yazarın baş harfleri. |
| dateTime | System::DateTime | Revizyonlar için kullanılacak tarih ve saat. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Akışlardan yüklenen iki belgeyi ek seçeneklerle karşılaştırır ve farkları belirtilen kaydetme formatında sağlanan çıkış akışına kaydeder, değişiklikleri bir dizi düzenleme ve format revizyonu olarak üretir.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Orijinal belge. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Değiştirilmiş belge. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveFormat | Aspose::Words::SaveFormat | Çıktının kaydetme biçimi. |
| yazar | const System::String\& | Revizyonlar için kullanılacak yazarın baş harfleri. |
| dateTime | System::DateTime | Revizyonlar için kullanılacak tarih ve saat. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) karşılaştırma seçenekleri. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) method


Akışlardan yüklenen iki belgeyi ek seçeneklerle karşılaştırır ve farkları belirtilen kaydetme formatında sağlanan çıkış akışına kaydeder, değişiklikleri bir dizi düzenleme ve format revizyonu olarak üretir.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Orijinal belge. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Değiştirilmiş belge. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Çıktının kaydetme seçenekleri. |
| yazar | const System::String\& | Revizyonlar için kullanılacak yazarın baş harfleri. |
| dateTime | System::DateTime | Revizyonlar için kullanılacak tarih ve saat. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Akışlardan yüklenen iki belgeyi ek seçeneklerle karşılaştırır ve farkları belirtilen kaydetme formatında sağlanan çıkış akışına kaydeder, değişiklikleri bir dizi düzenleme ve format revizyonu olarak üretir.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Orijinal belge. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Değiştirilmiş belge. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Çıktının kaydetme seçenekleri. |
| yazar | const System::String\& | Revizyonlar için kullanılacak yazarın baş harfleri. |
| dateTime | System::DateTime | Revizyonlar için kullanılacak tarih ve saat. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) karşılaştırma seçenekleri. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) method


İki belgeyi ek seçeneklerle karşılaştırır ve farkları sağlanan kaydetme formatında belirtilen çıkış dosyasına kaydeder, değişiklikleri bir dizi düzenleme ve format revizyonu olarak üretir.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| v1 | const System::String\& | Orijinal belge. |
| v2 | const System::String\& | Değiştirilmiş belge. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| saveFormat | Aspose::Words::SaveFormat | Çıktının kaydetme biçimi. |
| yazar | const System::String\& | Revizyonlar için kullanılacak yazarın baş harfleri. |
| dateTime | System::DateTime | Revizyonlar için kullanılacak tarih ve saat. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


İki belgeyi ek seçeneklerle karşılaştırır ve farkları sağlanan kaydetme formatında belirtilen çıkış dosyasına kaydeder, değişiklikleri bir dizi düzenleme ve format revizyonu olarak üretir.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| v1 | const System::String\& | Orijinal belge. |
| v2 | const System::String\& | Değiştirilmiş belge. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| saveFormat | Aspose::Words::SaveFormat | Çıktının kaydetme biçimi. |
| yazar | const System::String\& | Revizyonlar için kullanılacak yazarın baş harfleri. |
| dateTime | System::DateTime | Revizyonlar için kullanılacak tarih ve saat. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) karşılaştırma seçenekleri. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) method


İki belgeyi ek seçeneklerle karşılaştırır ve farkları sağlanan kaydetme formatında belirtilen çıkış dosyasına kaydeder, değişiklikleri bir dizi düzenleme ve format revizyonu olarak üretir.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| v1 | const System::String\& | Orijinal belge. |
| v2 | const System::String\& | Değiştirilmiş belge. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Çıktının kaydetme seçenekleri. |
| yazar | const System::String\& | Revizyonlar için kullanılacak yazarın baş harfleri. |
| dateTime | System::DateTime | Revizyonlar için kullanılacak tarih ve saat. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


İki belgeyi ek seçeneklerle karşılaştırır ve farkları sağlanan kaydetme formatında belirtilen çıkış dosyasına kaydeder, değişiklikleri bir dizi düzenleme ve format revizyonu olarak üretir.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| v1 | const System::String\& | Orijinal belge. |
| v2 | const System::String\& | Değiştirilmiş belge. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Çıktının kaydetme seçenekleri. |
| yazar | const System::String\& | Revizyonlar için kullanılacak yazarın baş harfleri. |
| dateTime | System::DateTime | Revizyonlar için kullanılacak tarih ve saat. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) karşılaştırma seçenekleri. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime) method


İki belgeyi ek seçeneklerle karşılaştırır ve farkları belirtilen çıkış dosyasına kaydeder, değişiklikleri bir dizi düzenleme ve format revizyonu olarak üretir.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::String &author, System::DateTime dateTime)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| v1 | const System::String\& | Orijinal belge. |
| v2 | const System::String\& | Değiştirilmiş belge. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| yazar | const System::String\& | Revizyonlar için kullanılacak yazarın baş harfleri. |
| dateTime | System::DateTime | Revizyonlar için kullanılacak tarih ve saat. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


İki belgeyi ek seçeneklerle karşılaştırır ve farkları belirtilen çıkış dosyasına kaydeder, değişiklikleri bir dizi düzenleme ve format revizyonu olarak üretir.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| v1 | const System::String\& | Orijinal belge. |
| v2 | const System::String\& | Değiştirilmiş belge. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| yazar | const System::String\& | Revizyonlar için kullanılacak yazarın baş harfleri. |
| dateTime | System::DateTime | Revizyonlar için kullanılacak tarih ve saat. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) karşılaştırma seçenekleri. |
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
