---
title: "Aspose::Words::LowCode::Converter::ConvertToImages yöntemi"
linktitle: "ConvertToImages"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::LowCode::Converter::ConvertToImages yöntemi. Belirtilen belgenin sayfalarını belirtilen formatta görüntülere dönüştürür ve C++'da görüntüleri içeren akışların bir dizisini döndürür."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.lowcode/converter/converttoimages/
---
## Converter::ConvertToImages(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::SaveFormat) method


Belirtilen belgenin sayfalarını belirtilen formatta görüntülere dönüştürür ve görüntüleri içeren akışların bir dizisini döndürür.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<Aspose::Words::Document> &doc, Aspose::Words::SaveFormat saveFormat)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doküman | const System::SharedPtr\<Aspose::Words::Document\>\& | Giriş belgesi. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme formatı. Yalnızca görüntü kaydetme formatlarına izin verilir. |

### ReturnValue

Görüntü akışlarının bir dizisini döndürür. Akışlar son kullanıcı tarafından serbest bırakılmalıdır.

## Ayrıca Bakınız

* Class [Document](../../../aspose.words/document/)
* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Belirtilen belgenin sayfalarını belirtilen kaydetme seçeneklerini kullanarak görüntülere dönüştürür ve görüntüleri içeren akışların bir dizisini döndürür.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<Aspose::Words::Document> &doc, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doküman | const System::SharedPtr\<Aspose::Words::Document\>\& | Giriş belgesi. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Görüntü kaydetme seçenekleri. |

### ReturnValue

Görüntü akışlarının bir dizisini döndürür. Akışlar son kullanıcı tarafından serbest bırakılmalıdır.

## Ayrıca Bakınız

* Class [Document](../../../aspose.words/document/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


Belirtilen giriş akışının sayfalarını belirtilen formatta görüntülere dönüştürür ve görüntüleri içeren akışların bir dizisini döndürür.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, Aspose::Words::SaveFormat saveFormat)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme formatı. Yalnızca görüntü kaydetme formatlarına izin verilir. |

### ReturnValue

Görüntü akışlarının bir dizisini döndürür. Akışlar son kullanıcı tarafından serbest bırakılmalıdır.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Belirtilen giriş akışının sayfalarını sağlanan yükleme ve kaydetme seçeneklerini kullanarak görüntülere dönüştürür ve görüntüleri içeren akışların bir dizisini döndürür.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Giriş belgesi yükleme seçenekleri. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Görüntü kaydetme seçenekleri. |

### ReturnValue

Görüntü akışlarının bir dizisini döndürür. Akışlar son kullanıcı tarafından serbest bırakılmalıdır.

## Ayrıca Bakınız

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Belirtilen giriş akışının sayfalarını belirtilen kaydetme seçeneklerini kullanarak görüntülere dönüştürür ve görüntüleri içeren akışların bir dizisini döndürür.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Görüntü kaydetme seçenekleri. |

### ReturnValue

Görüntü akışlarının bir dizisini döndürür. Akışlar son kullanıcı tarafından serbest bırakılmalıdır.

## Ayrıca Bakınız

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, Aspose::Words::SaveFormat) method


Belirtilen giriş dosyasının sayfalarını belirtilen formatta görüntülere dönüştürür ve görüntüleri içeren akışların bir dizisini döndürür.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, Aspose::Words::SaveFormat saveFormat)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFile | const System::String\& | Girdi dosya adı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme formatı. Yalnızca görüntü kaydetme formatlarına izin verilir. |

### ReturnValue

Görüntü akışlarının bir dizisini döndürür. Akışlar son kullanıcı tarafından serbest bırakılmalıdır.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Belirtilen giriş dosyasının sayfalarını sağlanan yükleme ve kaydetme seçeneklerini kullanarak görüntü dosyalarına dönüştürür.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFile | const System::String\& | Girdi dosya adı. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Giriş belgesi yükleme seçenekleri. |
| outputFile | const System::String\& | Sayfa görüntüleri için dosya adı oluşturmak amacıyla kullanılan çıkış dosya adı, "outputFile_pageIndex.extension" kuralını kullanır. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Görüntü kaydetme seçenekleri. |

## Ayrıca Bakınız

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Belirtilen giriş dosyasının sayfalarını belirtilen kaydetme seçeneklerini kullanarak görüntülere dönüştürür ve görüntüleri içeren akışların bir dizisini döndürür.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFile | const System::String\& | Girdi dosya adı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Görüntü kaydetme seçenekleri. |

### ReturnValue

Görüntü akışlarının bir dizisini döndürür. Akışlar son kullanıcı tarafından serbest bırakılmalıdır.

## Ayrıca Bakınız

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&) method


Belirtilen giriş dosyasının sayfalarını görüntü dosyalarına dönüştürür.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFile | const System::String\& | Girdi dosya adı. |
| outputFile | const System::String\& | Sayfa görüntüleri için dosya adı oluşturmak amacıyla kullanılan çıkış dosya adı, "outputFile_pageIndex.extension" kuralını kullanır. |

## Ayrıca Bakınız

* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) method


Belirtilen giriş dosyasının sayfalarını belirtilen formatta görüntü dosyalarına dönüştürür.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile, Aspose::Words::SaveFormat saveFormat)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFile | const System::String\& | Girdi dosya adı. |
| outputFile | const System::String\& | Sayfa görüntüleri için dosya adı oluşturmak amacıyla kullanılan çıkış dosya adı, "outputFile_pageIndex.extension" kuralını kullanır. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme formatı. Yalnızca görüntü kaydetme formatlarına izin verilir. |

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Belirtilen giriş dosyasının sayfalarını belirtilen kaydetme seçeneklerini kullanarak görüntü dosyalarına dönüştürür.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFile | const System::String\& | Girdi dosya adı. |
| outputFile | const System::String\& | Sayfa görüntüleri için dosya adı oluşturmak amacıyla kullanılan çıkış dosya adı, "outputFile_pageIndex.extension" kuralını kullanır. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Görüntü kaydetme seçenekleri. |

## Ayrıca Bakınız

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
