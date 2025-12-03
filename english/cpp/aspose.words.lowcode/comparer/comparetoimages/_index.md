---
title: Aspose::Words::LowCode::Comparer::CompareToImages method
linktitle: CompareToImages
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LowCode::Comparer::CompareToImages method. Compares two documents and saves the differences as images. Each item in the returned array represents a single page of the output rendered as an image in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.lowcode/comparer/comparetoimages/
---
## Comparer::CompareToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) method


Compares two documents and saves the differences as images. Each item in the returned array represents a single page of the output rendered as an image.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Comparer::CompareToImages(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &imageSaveOptions, const System::String &author, System::DateTime dateTime)
```


| Parameter | Type | Description |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | The original document. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | The modified document. |
| imageSaveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | The output's image save options. |
| author | const System::String\& | Initials of the author to use for revisions. |
| dateTime | System::DateTime | The date and time to use for revisions. |

## See Also

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::CompareToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Compares two documents and saves the differences as images. Each item in the returned array represents a single page of the output rendered as an image.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Comparer::CompareToImages(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &imageSaveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | The original document. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | The modified document. |
| imageSaveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | The output's image save options. |
| author | const System::String\& | Initials of the author to use for revisions. |
| dateTime | System::DateTime | The date and time to use for revisions. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) comparison options. |

## See Also

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::CompareToImages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) method


Compares two documents and saves the differences as images. Each item in the returned array represents a single page of the output rendered as an image.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Comparer::CompareToImages(const System::String &v1, const System::String &v2, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &imageSaveOptions, const System::String &author, System::DateTime dateTime)
```


| Parameter | Type | Description |
| --- | --- | --- |
| v1 | const System::String\& | The original document. |
| v2 | const System::String\& | The modified document. |
| imageSaveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | The output's image save options. |
| author | const System::String\& | Initials of the author to use for revisions. |
| dateTime | System::DateTime | The date and time to use for revisions. |

## See Also

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::CompareToImages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Compares two documents and saves the differences as images. Each item in the returned array represents a single page of the output rendered as an image.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Comparer::CompareToImages(const System::String &v1, const System::String &v2, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &imageSaveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| v1 | const System::String\& | The original document. |
| v2 | const System::String\& | The modified document. |
| imageSaveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | The output's image save options. |
| author | const System::String\& | Initials of the author to use for revisions. |
| dateTime | System::DateTime | The date and time to use for revisions. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) comparison options. |

## See Also

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
