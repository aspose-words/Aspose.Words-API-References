---
title: Aspose::Words::LowCode::Converter::ConvertToImages method
linktitle: ConvertToImages
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LowCode::Converter::ConvertToImages method. Converts the pages of the specified document to images in the specified format and returns an array of streams containing the images in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.lowcode/converter/converttoimages/
---
## Converter::ConvertToImages(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::SaveFormat) method


Converts the pages of the specified document to images in the specified format and returns an array of streams containing the images.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<Aspose::Words::Document> &doc, Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::Document\>\& | The input document. |
| saveFormat | Aspose::Words::SaveFormat | Save format. Only image save formats are allowed. |

### ReturnValue

Returns array of image streams. The streams should be disposed by the end user.

## See Also

* Class [Document](../../../aspose.words/document/)
* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Converts the pages of the specified document to images using the specified save options and returns an array of streams containing the images.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<Aspose::Words::Document> &doc, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::Document\>\& | The input document. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Image save options. |

### ReturnValue

Returns array of image streams. The streams should be disposed by the end user.

## See Also

* Class [Document](../../../aspose.words/document/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


Converts the pages of the specified input stream to images in the specified format and returns an array of streams containing the images.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | The input stream. |
| saveFormat | Aspose::Words::SaveFormat | Save format. Only image save formats are allowed. |

### ReturnValue

Returns array of image streams. The streams should be disposed by the end user.

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Converts the pages of the specified input stream to images using the provided load and save options, and returns an array of streams containing the images.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | The input stream. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | The input document load options. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Image save options. |

### ReturnValue

Returns array of image streams. The streams should be disposed by the end user.

## See Also

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Converts the pages of the specified input stream to images using the specified save options and returns an array of streams containing the images.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | The input stream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Image save options. |

### ReturnValue

Returns array of image streams. The streams should be disposed by the end user.

## See Also

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, Aspose::Words::SaveFormat) method


Converts the pages of the specified input file to images in the specified format and returns an array of streams containing the images.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | const System::String\& | The input file name. |
| saveFormat | Aspose::Words::SaveFormat | Save format. Only image save formats are allowed. |

### ReturnValue

Returns array of image streams. The streams should be disposed by the end user.

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Converts the pages of the specified input file to image files using the provided load and save options.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | const System::String\& | The input file name. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | The input document load options. |
| outputFile | const System::String\& | The output file name used to generate file name for page images using rule "outputFile_pageIndex.extension" |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Image save options. |

## See Also

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Converts the pages of the specified input file to images using the specified save options and returns an array of streams containing the images.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | const System::String\& | The input file name. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Image save options. |

### ReturnValue

Returns array of image streams. The streams should be disposed by the end user.

## See Also

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&) method


Converts the pages of the specified input file to image files.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | const System::String\& | The input file name. |
| outputFile | const System::String\& | The output file name used to generate file name for page images using rule "outputFile_pageIndex.extension" |

## See Also

* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) method


Converts the pages of the specified input file to image files in the specified format.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile, Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | const System::String\& | The input file name. |
| outputFile | const System::String\& | The output file name used to generate file name for page images using rule "outputFile_pageIndex.extension" |
| saveFormat | Aspose::Words::SaveFormat | Save format. Only image save formats are allowed. |

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Converts the pages of the specified input file to image files using the specified save options.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | const System::String\& | The input file name. |
| outputFile | const System::String\& | The output file name used to generate file name for page images using rule "outputFile_pageIndex.extension" |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Image save options. |

## See Also

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
