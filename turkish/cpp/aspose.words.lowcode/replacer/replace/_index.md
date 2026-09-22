---
title: "Aspose::Words::LowCode::Replacer::Replace yöntemi"
linktitle: "Değiştir"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::LowCode::Replacer::Replace yöntemi. Belirtilen bir karakter dizesi kalıbının tüm eşleşmelerini, düzenli ifade kullanarak giriş akışında bir değiştirme dizesiyle, belirtilen kaydetme formatı ve ek seçeneklerle C++'ta değiştirir."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.lowcode/replacer/replace/
---
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Belirtilen karakter dizi deseninin tüm oluşumlarını, belirtilen kaydetme formatı ve ek seçeneklerle, bir düzenli ifade kullanarak giriş akışında bir değiştirme dizesiyle değiştirir.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |
| desen | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Eşleşmeleri bulmak için kullanılan bir düzenli ifade deseni. |
| değiştirme | const System::String\& | Desenin tüm eşleşmelerini değiştirmek için bir dize. |

### ReturnValue

Yapılan değiştirme sayısı.
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Belirtilen karakter dizi deseninin tüm oluşumlarını, belirtilen kaydetme formatı ve ek seçeneklerle, bir düzenli ifade kullanarak giriş akışında bir değiştirme dizesiyle değiştirir.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |
| desen | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Eşleşmeleri bulmak için kullanılan bir düzenli ifade deseni. |
| değiştirme | const System::String\& | Desenin tüm eşleşmelerini değiştirmek için bir dize. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) nesnesi ek seçenekleri belirtmek için. |

### ReturnValue

Yapılan değiştirme sayısı.
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) method


Belirtilen karakter dizesi deseninin tüm oluşumlarını giriş akışında, belirtilen kaydetme formatı ve ek seçeneklerle bir değiştirme dizesiyle değiştirir.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |
| desen | const System::String\& | Değiştirilecek bir dize. |
| değiştirme | const System::String\& | Desenin tüm eşleşmelerini değiştirmek için bir dize. |

### ReturnValue

Yapılan değiştirme sayısı.
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Belirtilen karakter dizesi deseninin tüm oluşumlarını giriş akışında, belirtilen kaydetme formatı ve ek seçeneklerle bir değiştirme dizesiyle değiştirir.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |
| desen | const System::String\& | Değiştirilecek bir dize. |
| değiştirme | const System::String\& | Desenin tüm eşleşmelerini değiştirmek için bir dize. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) nesnesi ek seçenekleri belirtmek için. |

### ReturnValue

Yapılan değiştirme sayısı.
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Belirtilen karakter dizi deseninin tüm oluşumlarını, belirtilen kaydetme formatı ve ek seçeneklerle, bir düzenli ifade kullanarak giriş akışında bir değiştirme dizesiyle değiştirir.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
| desen | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Eşleşmeleri bulmak için kullanılan bir düzenli ifade deseni. |
| değiştirme | const System::String\& | Desenin tüm eşleşmelerini değiştirmek için bir dize. |

### ReturnValue

Yapılan değiştirme sayısı.
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Belirtilen karakter dizi deseninin tüm oluşumlarını, belirtilen kaydetme formatı ve ek seçeneklerle, bir düzenli ifade kullanarak giriş akışında bir değiştirme dizesiyle değiştirir.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
| desen | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Eşleşmeleri bulmak için kullanılan bir düzenli ifade deseni. |
| değiştirme | const System::String\& | Desenin tüm eşleşmelerini değiştirmek için bir dize. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) nesnesi ek seçenekleri belirtmek için. |

### ReturnValue

Yapılan değiştirme sayısı.
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) method


Belirtilen karakter dizesi deseninin tüm oluşumlarını giriş akışında, belirtilen kaydetme formatı ve ek seçeneklerle bir değiştirme dizesiyle değiştirir.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
| desen | const System::String\& | Değiştirilecek bir dize. |
| değiştirme | const System::String\& | Desenin tüm eşleşmelerini değiştirmek için bir dize. |

### ReturnValue

Yapılan değiştirme sayısı.
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Belirtilen karakter dizesi deseninin tüm oluşumlarını giriş akışında, belirtilen kaydetme formatı ve ek seçeneklerle bir değiştirme dizesiyle değiştirir.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Giriş akışı. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Çıktı akışı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
| desen | const System::String\& | Değiştirilecek bir dize. |
| değiştirme | const System::String\& | Desenin tüm eşleşmelerini değiştirmek için bir dize. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) nesnesi ek seçenekleri belirtmek için. |

### ReturnValue

Yapılan değiştirme sayısı.
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının yalnızca ilk sayfası belirtilen akışa kaydedilir.

Çıktı biçimi TIFF ise, çıktı belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Belirtilen karakter dizi deseninin tüm oluşumlarını, belirtilen kaydetme formatı ve ek seçeneklerle, bir düzenli ifade kullanarak giriş dosyasında bir değiştirme dizesiyle değiştirir.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |
| desen | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Eşleşmeleri bulmak için kullanılan bir düzenli ifade deseni. |
| değiştirme | const System::String\& | Desenin tüm eşleşmelerini değiştirmek için bir dize. |

### ReturnValue

Yapılan değiştirme sayısı.
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Belirtilen karakter dizi deseninin tüm oluşumlarını, belirtilen kaydetme formatı ve ek seçeneklerle, bir düzenli ifade kullanarak giriş dosyasında bir değiştirme dizesiyle değiştirir.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |
| desen | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Eşleşmeleri bulmak için kullanılan bir düzenli ifade deseni. |
| değiştirme | const System::String\& | Desenin tüm eşleşmelerini değiştirmek için bir dize. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) nesnesi ek seçenekleri belirtmek için. |

### ReturnValue

Yapılan değiştirme sayısı.
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) method


Belirtilen karakter dizesi deseninin tüm oluşumlarını giriş dosyasında, belirtilen kaydetme formatı ve ek seçeneklerle bir değiştirme dizesiyle değiştirir.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |
| desen | const System::String\& | Değiştirilecek bir dize. |
| değiştirme | const System::String\& | Desenin tüm eşleşmelerini değiştirmek için bir dize. |

### ReturnValue

Yapılan değiştirme sayısı.
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Belirtilen karakter dizesi deseninin tüm oluşumlarını giriş dosyasında, belirtilen kaydetme formatı ve ek seçeneklerle bir değiştirme dizesiyle değiştirir.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme biçimi. |
| desen | const System::String\& | Değiştirilecek bir dize. |
| değiştirme | const System::String\& | Desenin tüm eşleşmelerini değiştirmek için bir dize. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) nesnesi ek seçenekleri belirtmek için. |

### ReturnValue

Yapılan değiştirme sayısı.
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Belirtilen karakter dizi deseninin tüm oluşumlarını, belirtilen kaydetme formatı ve ek seçeneklerle, bir düzenli ifade kullanarak giriş dosyasında bir değiştirme dizesiyle değiştirir.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
| desen | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Eşleşmeleri bulmak için kullanılan bir düzenli ifade deseni. |
| değiştirme | const System::String\& | Desenin tüm eşleşmelerini değiştirmek için bir dize. |

### ReturnValue

Yapılan değiştirme sayısı.
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Belirtilen karakter dizi deseninin tüm oluşumlarını, belirtilen kaydetme formatı ve ek seçeneklerle, bir düzenli ifade kullanarak giriş dosyasında bir değiştirme dizesiyle değiştirir.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
| desen | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Eşleşmeleri bulmak için kullanılan bir düzenli ifade deseni. |
| değiştirme | const System::String\& | Desenin tüm eşleşmelerini değiştirmek için bir dize. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) nesnesi ek seçenekleri belirtmek için. |

### ReturnValue

Yapılan değiştirme sayısı.
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) method


Belirtilen karakter dizesi deseninin tüm oluşumlarını giriş dosyasında, belirtilen kaydetme formatı ve ek seçeneklerle bir değiştirme dizesiyle değiştirir.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
| desen | const System::String\& | Değiştirilecek bir dize. |
| değiştirme | const System::String\& | Desenin tüm eşleşmelerini değiştirmek için bir dize. |

### ReturnValue

Yapılan değiştirme sayısı.
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Belirtilen karakter dizesi deseninin tüm oluşumlarını giriş dosyasında, belirtilen kaydetme formatı ve ek seçeneklerle bir değiştirme dizesiyle değiştirir.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Kaydetme seçenekleri. |
| desen | const System::String\& | Değiştirilecek bir dize. |
| değiştirme | const System::String\& | Desenin tüm eşleşmelerini değiştirmek için bir dize. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) nesnesi ek seçenekleri belirtmek için. |

### ReturnValue

Yapılan değiştirme sayısı.
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Belirtilen karakter dizesi deseninin tüm oluşumlarını giriş dosyasında düzenli ifade kullanarak bir değiştirme dizesiyle değiştirir.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| desen | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Eşleşmeleri bulmak için kullanılan bir düzenli ifade deseni. |
| değiştirme | const System::String\& | Desenin tüm eşleşmelerini değiştirmek için bir dize. |

### ReturnValue

Yapılan değiştirme sayısı.
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::String\&, const System::String\&) method


Belirtilen karakter dizesi deseninin tüm oluşumlarını giriş dosyasında bir değiştirme dizesiyle değiştirir.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::String &pattern, const System::String &replacement)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | const System::String\& | Girdi dosya adı. |
| outputFileName | const System::String\& | Çıktı dosya adı. |
| desen | const System::String\& | Değiştirilecek bir dize. |
| değiştirme | const System::String\& | Desenin tüm eşleşmelerini değiştirmek için bir dize. |

### ReturnValue

Yapılan değiştirme sayısı.
## Açıklamalar


Çıktı biçimi bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıktı biçimi TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Ayrıca Bakınız

* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
