---
title: Aspose::Words::LowCode::Comparer::Compare method
linktitle: Compare
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LowCode::Comparer::Compare method. Compares two documents loaded from streams with additional options and saves the differences to the provided output stream in the specified save format, producing changes as a number of edit and format revisions in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.lowcode/comparer/compare/
---
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) method


Compares two documents loaded from streams with additional options and saves the differences to the provided output stream in the specified save format, producing changes as a number of edit and format revisions.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime)
```


| Parameter | Type | Description |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | The original document. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | The modified document. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | The output stream. |
| saveFormat | Aspose::Words::SaveFormat | The output's save format. |
| author | const System::String\& | Initials of the author to use for revisions. |
| dateTime | System::DateTime | The date and time to use for revisions. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), only the first page of the output will be saved to the specified stream.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF to the specified stream.

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Compares two documents loaded from streams with additional options and saves the differences to the provided output stream in the specified save format, producing changes as a number of edit and format revisions.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | The original document. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | The modified document. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | The output stream. |
| saveFormat | Aspose::Words::SaveFormat | The output's save format. |
| author | const System::String\& | Initials of the author to use for revisions. |
| dateTime | System::DateTime | The date and time to use for revisions. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) comparison options. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), only the first page of the output will be saved to the specified stream.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF to the specified stream.

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) method


Compares two documents loaded from streams with additional options and saves the differences to the provided output stream in the specified save format, producing changes as a number of edit and format revisions.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime)
```


| Parameter | Type | Description |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | The original document. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | The modified document. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | The output stream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | The output's save options. |
| author | const System::String\& | Initials of the author to use for revisions. |
| dateTime | System::DateTime | The date and time to use for revisions. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), only the first page of the output will be saved to the specified stream.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF to the specified stream.

## See Also

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Compares two documents loaded from streams with additional options and saves the differences to the provided output stream in the specified save format, producing changes as a number of edit and format revisions.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | The original document. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | The modified document. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | The output stream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | The output's save options. |
| author | const System::String\& | Initials of the author to use for revisions. |
| dateTime | System::DateTime | The date and time to use for revisions. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) comparison options. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), only the first page of the output will be saved to the specified stream.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF to the specified stream.

## See Also

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) method


Compares two documents with additional options and saves the differences to the specified output file in the provided save format, producing changes as a number of edit and format revisions.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime)
```


| Parameter | Type | Description |
| --- | --- | --- |
| v1 | const System::String\& | The original document. |
| v2 | const System::String\& | The modified document. |
| outputFileName | const System::String\& | The output file name. |
| saveFormat | Aspose::Words::SaveFormat | The output's save format. |
| author | const System::String\& | Initials of the author to use for revisions. |
| dateTime | System::DateTime | The date and time to use for revisions. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Compares two documents with additional options and saves the differences to the specified output file in the provided save format, producing changes as a number of edit and format revisions.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| v1 | const System::String\& | The original document. |
| v2 | const System::String\& | The modified document. |
| outputFileName | const System::String\& | The output file name. |
| saveFormat | Aspose::Words::SaveFormat | The output's save format. |
| author | const System::String\& | Initials of the author to use for revisions. |
| dateTime | System::DateTime | The date and time to use for revisions. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) comparison options. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) method


Compares two documents with additional options and saves the differences to the specified output file in the provided save format, producing changes as a number of edit and format revisions.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime)
```


| Parameter | Type | Description |
| --- | --- | --- |
| v1 | const System::String\& | The original document. |
| v2 | const System::String\& | The modified document. |
| outputFileName | const System::String\& | The output file name. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | The output's save options. |
| author | const System::String\& | Initials of the author to use for revisions. |
| dateTime | System::DateTime | The date and time to use for revisions. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

## See Also

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Compares two documents with additional options and saves the differences to the specified output file in the provided save format, producing changes as a number of edit and format revisions.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| v1 | const System::String\& | The original document. |
| v2 | const System::String\& | The modified document. |
| outputFileName | const System::String\& | The output file name. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | The output's save options. |
| author | const System::String\& | Initials of the author to use for revisions. |
| dateTime | System::DateTime | The date and time to use for revisions. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) comparison options. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

## See Also

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime) method


Compares two documents with additional options and saves the differences to the specified output file, producing changes as a number of edit and format revisions.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::String &author, System::DateTime dateTime)
```


| Parameter | Type | Description |
| --- | --- | --- |
| v1 | const System::String\& | The original document. |
| v2 | const System::String\& | The modified document. |
| outputFileName | const System::String\& | The output file name. |
| author | const System::String\& | Initials of the author to use for revisions. |
| dateTime | System::DateTime | The date and time to use for revisions. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

## See Also

* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Compares two documents with additional options and saves the differences to the specified output file, producing changes as a number of edit and format revisions.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| v1 | const System::String\& | The original document. |
| v2 | const System::String\& | The modified document. |
| outputFileName | const System::String\& | The output file name. |
| author | const System::String\& | Initials of the author to use for revisions. |
| dateTime | System::DateTime | The date and time to use for revisions. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) comparison options. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

## See Also

* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
