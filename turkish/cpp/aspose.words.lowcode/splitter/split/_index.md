---
title: "Aspose::Words::LowCode::Splitter::Split yöntemi"
linktitle: "Böl"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::LowCode::Splitter::Split yöntemi. Belirtilen bölme seçeneklerine göre bir girdi akışından belgeyi birden çok parçaya böler ve sonuç parçaları belirtilen kaydetme biçiminde akışlar dizisi olarak döndürür C++'ta."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.lowcode/splitter/split/
---
## Splitter::Split(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Bir giriş akışındaki belgeyi belirtilen bölme seçeneklerine göre birden çok parçaya ayırır ve ortaya çıkan parçaları belirtilen kaydetme formatında akış dizisi olarak döndürür.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Splitter::Split(const System::SharedPtr<System::IO::Stream> &inputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) bölme seçenekleri. |

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Bir giriş akışındaki belgeyi belirtilen bölme seçeneklerine göre birden çok parçaya ayırır ve ortaya çıkan parçaları belirtilen kaydetme formatında akış dizisi olarak döndürür.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Splitter::Split(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) bölme seçenekleri. |

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Belgeyi belirtilen bölme seçeneklerine göre birden çok parçaya ayırır ve ortaya çıkan parçaları belirtilen kaydetme formatında dosyalara kaydeder.

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Kural "outputFile_partIndex.extension" kullanılarak belge parçaları için dosya adı oluşturmakta kullanılan çıktı dosyası adı |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) bölme seçenekleri. |

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Belgeyi belirtilen bölme seçeneklerine göre birden çok parçaya ayırır ve ortaya çıkan parçaları dosyalara kaydeder. Çıktı dosya formatı, çıktı dosya adının uzantısına göre belirlenir.

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Kural "outputFile_partIndex.extension" kullanılarak belge parçaları için dosya adı oluşturmakta kullanılan çıktı dosyası adı |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) bölme seçenekleri. |

## Ayrıca Bakınız

* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Belgeyi belirtilen bölme seçeneklerine göre birden çok parçaya ayırır ve ortaya çıkan parçaları belirtilen kaydetme formatında dosyalara kaydeder.

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Kural "outputFile_partIndex.extension" kullanılarak belge parçaları için dosya adı oluşturmakta kullanılan çıktı dosyası adı |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) bölme seçenekleri. |

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
