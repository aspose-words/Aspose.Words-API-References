---
title: Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream method
linktitle: get_DocumentPartStream
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream method. Allows to specify the stream where the document part will be saved to in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.saving/documentpartsavingargs/get_documentpartstream/
---
## DocumentPartSavingArgs::get_DocumentPartStream method


Allows to specify the stream where the document part will be saved to.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream() const
```

## Remarks


This property allows you to save document parts to streams instead of files during HTML export.

The default value is **null**. When this property is **null**, the document part will be saved to a file specified in the [DocumentPartFileName](../get_documentpartfilename/) property.

When saving to a stream in HTML format is requested by [Save()](../) or [Save()](../) and first document part is about to be saved, Aspose.Words suggests here the main output stream initially passed by the caller.

When saving to EPUB format that is a container format based on HTML, [DocumentPartStream](./) cannot be specified because all subsidiary parts will be encapsulated into a single output package.

## See Also

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
