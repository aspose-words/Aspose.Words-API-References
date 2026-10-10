---
title: "Aspose::Words::LowCode::Splitter::ExtractPages yöntemi"
linktitle: "ExtractPages"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::LowCode::Splitter::ExtractPages yöntemi. Belirtilen bir sayfa aralığını belge akışından çıkarır ve çıkarılan sayfaları belirtilen kaydetme biçiminde bir çıktı akışına kaydeder C++'ta."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.lowcode/splitter/extractpages/
---
## Splitter::ExtractPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, int32_t, int32_t) method


Belge akışından belirtilen bir sayfa aralığını çıkarır ve çıkarılan sayfaları belirtilen kaydetme formatını kullanarak bir çıktı akışına kaydeder.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, int32_t startPageIndex, int32_t pageCount)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |
| startPageIndex | int32_t | Çıkarılacak ilk sayfanın sıfır tabanlı indeksi. |
| pageCount | int32_t | Çıkarılacak sayfa sayısı. |

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) method


Belge akışından belirtilen bir sayfa aralığını çıkarır ve çıkarılan sayfaları belirtilen kaydetme formatını kullanarak bir çıktı akışına kaydeder.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, int32_t startPageIndex, int32_t pageCount)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
| startPageIndex | int32_t | Çıkarılacak ilk sayfanın sıfır tabanlı indeksi. |
| pageCount | int32_t | Çıkarılacak sayfa sayısı. |

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, int32_t, int32_t) method


Belge dosyasından belirtilen bir sayfa aralığını çıkarır ve çıkarılan sayfaları belirtilen kaydetme formatını kullanarak yeni bir dosyaya kaydeder.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, int32_t startPageIndex, int32_t pageCount)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |
| startPageIndex | int32_t | Çıkarılacak ilk sayfanın sıfır tabanlı indeksi. |
| pageCount | int32_t | Çıkarılacak sayfa sayısı. |

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) method


Belge dosyasından belirtilen bir sayfa aralığını çıkarır ve çıkarılan sayfaları belirtilen kaydetme formatını kullanarak yeni bir dosyaya kaydeder.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, int32_t startPageIndex, int32_t pageCount)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
| startPageIndex | int32_t | Çıkarılacak ilk sayfanın sıfır tabanlı indeksi. |
| pageCount | int32_t | Çıkarılacak sayfa sayısı. |

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, int32_t, int32_t) method


Belge dosyasından belirtilen bir sayfa aralığını çıkarır ve çıkarılan sayfaları yeni bir dosyaya kaydeder. Çıktı dosya formatı, çıktı dosya adının uzantısına göre belirlenir.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, int32_t startPageIndex, int32_t pageCount)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| startPageIndex | int32_t | Çıkarılacak ilk sayfanın sıfır tabanlı indeksi. |
| pageCount | int32_t | Çıkarılacak sayfa sayısı. |

## Ayrıca Bakınız

* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
