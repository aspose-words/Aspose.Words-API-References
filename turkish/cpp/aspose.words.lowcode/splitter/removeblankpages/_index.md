---
title: "Aspose::Words::LowCode::Splitter::RemoveBlankPages yöntemi"
linktitle: "RemoveBlankPages"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::LowCode::Splitter::RemoveBlankPages yöntemi. Girdi akışında sağlanan bir belgeden boş sayfaları kaldırır ve güncellenen belgeyi belirtilen kaydetme formatında bir çıktı akışına kaydeder. C++'de kaldırılan sayfa numaralarının bir listesini döndürür."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.lowcode/splitter/removeblankpages/
---
## Splitter::RemoveBlankPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


Giriş akışında sağlanan bir belgedeki boş sayfaları kaldırır ve güncellenen belgeyi belirtilen kaydetme formatında bir çıktı akışına kaydeder. Kaldırılan sayfa numaralarının bir listesini döndürür.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |

### ReturnValue

Sayfa numaraları listesi boş olarak kabul edildi ve kaldırıldı.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Giriş akışında sağlanan bir belgedeki boş sayfaları kaldırır ve güncellenen belgeyi belirtilen kaydetme formatında bir çıktı akışına kaydeder. Kaldırılan sayfa numaralarının bir listesini döndürür.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |

### ReturnValue

Sayfa numaraları listesi boş olarak kabul edildi ve kaldırıldı.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::String\&, const System::String\&) method


Belgedeki boş sayfaları kaldırır ve çıktıyı kaydeder. Kaldırılan sayfa numaralarının bir listesini döndürür.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::String &inputFileName, const System::String &outputFileName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |

### ReturnValue

Sayfa numaraları listesi boş olarak kabul edildi ve kaldırıldı.

## Ayrıca Bakınız

* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) method


Belgedeki boş sayfaları kaldırır ve çıktıyı belirtilen formatta kaydeder. Kaldırılan sayfa numaralarının bir listesini döndürür.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |

### ReturnValue

Sayfa numaraları listesi boş olarak kabul edildi ve kaldırıldı.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Belgedeki boş sayfaları kaldırır ve çıktıyı belirtilen formatta kaydeder. Kaldırılan sayfa numaralarının bir listesini döndürür.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |

### ReturnValue

Sayfa numaraları listesi boş olarak kabul edildi ve kaldırıldı.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
