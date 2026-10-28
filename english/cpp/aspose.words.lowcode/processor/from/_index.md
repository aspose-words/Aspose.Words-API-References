---
title: Aspose::Words::LowCode::Processor::From method
linktitle: From
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LowCode::Processor::From method. Specifies input document for processing in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.lowcode/processor/from/
---
## Processor::From(const System::SharedPtr\<System::IO::Stream\> \&) method


Specifies input document for processing.

```cpp
System::SharedPtr<Aspose::Words::LowCode::Processor> Aspose::Words::LowCode::Processor::From(const System::SharedPtr<System::IO::Stream> & input)
```


| Parameter | Type | Description |
| --- | --- | --- |
| input | const System::SharedPtr\<System::IO::Stream\> \& | Input document stream. |

### ReturnValue

Returns processor with specified input file stream.
## Remarks

 If the processor accepts only one file as an input, only the last specified file will be processed. [Merger](../../merger/) processor accepts multiple files as an input, as the result all the specified documents will be merged. [Converter](../../converter/) processor accepts only one file as an input, so only the last specified file will be converted. 
## See Also

* Class [Processor](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Processor::From(const System::SharedPtr\<System::IO::Stream\> \&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> \&) method


Specifies input document for processing.

```cpp
System::SharedPtr<Aspose::Words::LowCode::Processor> Aspose::Words::LowCode::Processor::From(const System::SharedPtr<System::IO::Stream> & input, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> & loadOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| input | const System::SharedPtr\<System::IO::Stream\> \& | Input document stream. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> \& | Optional load options used to load the document. |

### ReturnValue

Returns processor with specified input file stream.
## Remarks

 If the processor accepts only one file as an input, only the last specified file will be processed. [Merger](../../merger/) processor accepts multiple files as an input, as the result all the specified documents will be merged. [Converter](../../converter/) processor accepts only one file as an input, so only the last specified file will be converted. 
## See Also

* Class [Processor](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Processor::From(const System::String \&) method


Specifies input document for processing.

```cpp
System::SharedPtr<Aspose::Words::LowCode::Processor> Aspose::Words::LowCode::Processor::From(const System::String & input)
```


| Parameter | Type | Description |
| --- | --- | --- |
| input | const System::String \& | Input document file name. |

### ReturnValue

Returns processor with specified input file.
## Remarks

 If the processor accepts only one file as an input, only the last specified file will be processed. [Merger](../../merger/) processor accepts multiple files as an input, as the result all the specified documents will be merged. [Converter](../../converter/) processor accepts only one file as an input, so only the last specified file will be converted. 
## See Also

* Class [Processor](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Processor::From(const System::String \&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> \&) method


Specifies input document for processing.

```cpp
System::SharedPtr<Aspose::Words::LowCode::Processor> Aspose::Words::LowCode::Processor::From(const System::String & input, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> & loadOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| input | const System::String \& | Input document file name. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> \& | Optional load options used to load the document. |

### ReturnValue

Returns processor with specified input file.
## Remarks

 If the processor accepts only one file as an input, only the last specified file will be processed. [Merger](../../merger/) processor accepts multiple files as an input, as the result all the specified documents will be merged. [Converter](../../converter/) processor accepts only one file as an input, so only the last specified file will be converted. 
## See Also

* Class [Processor](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
