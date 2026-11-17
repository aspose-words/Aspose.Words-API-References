---
title: Aspose::Words::Saving::DocumentPartSavingArgs::set_DocumentPartStream method
linktitle: set_DocumentPartStream
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::DocumentPartSavingArgs::set_DocumentPartStream method. Allows to specify the stream where the document part will be saved to in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.saving/documentpartsavingargs/set_documentpartstream/
---
## DocumentPartSavingArgs::set_DocumentPartStream(const System::SharedPtr\<System::IO::Stream\> \&) method


Allows to specify the stream where the document part will be saved to.

```cpp
void Aspose::Words::Saving::DocumentPartSavingArgs::set_DocumentPartStream(const System::SharedPtr<System::IO::Stream> & value)
```

## Remarks


This property allows you to save document parts to streams instead of files during HTML export.

The default value is **null**. When this property is **null**, the document part will be saved to a file specified in the [DocumentPartFileName](../get_documentpartfilename/) property.

When saving to a stream in HTML format is requested by [Save()](../../../aspose.words/document/save/) or [Save()](../../../aspose.words/document/save/) and first document part is about to be saved, Aspose.Words suggests here the main output stream initially passed by the caller.

When saving to EPUB format that is a container format based on HTML, [DocumentPartStream](../get_documentpartstream/) cannot be specified because all subsidiary parts will be encapsulated into a single output package.
## See Also

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentPartSavingArgs::set_DocumentPartStream(std::basic_ostream\<CharType, Traits\> \&) method


Allows to specify the stream where the document part will be saved to.

```cpp
template<typename CharType,typename Traits> void Aspose::Words::Saving::DocumentPartSavingArgs::set_DocumentPartStream(std::basic_ostream<CharType, Traits> & value)
```

## Remarks


This property allows you to save document parts to streams instead of files during HTML export.

The default value is **null**. When this property is **null**, the document part will be saved to a file specified in the [DocumentPartFileName](../get_documentpartfilename/) property.

When saving to a stream in HTML format is requested by [Save()](../../../aspose.words/document/save/) or [Save()](../../../aspose.words/document/save/) and first document part is about to be saved, Aspose.Words suggests here the main output stream initially passed by the caller.

When saving to EPUB format that is a container format based on HTML, [DocumentPartStream](../get_documentpartstream/) cannot be specified because all subsidiary parts will be encapsulated into a single output package.
## See Also

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
