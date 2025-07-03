---
title: Aspose::Words::Saving::SaveOptions::get_TempFolder method
linktitle: get_TempFolder
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::SaveOptions::get_TempFolder method. Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is null and no temporary files are used in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words.saving/saveoptions/get_tempfolder/
---
## SaveOptions::get_TempFolder method


Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is **null** and no temporary files are used.

```cpp
System::String Aspose::Words::Saving::SaveOptions::get_TempFolder() const
```

## Remarks


When Aspose.Words saves a document, it needs to create temporary internal structures. By default, these internal structures are created in memory and the memory usage spikes for a short period while the document is being saved. When saving is complete, the memory is freed and reclaimed by the garbage collector.

Specifying a temporary folder using [TempFolder](./) will cause Aspose.Words to keep the internal structures in temporary files instead of memory. It reduces the memory usage during saving, but will decrease the save performance.

The folder must exist and be writable, otherwise an exception will be thrown.

Aspose.Words automatically deletes all temporary files when saving is complete.

## Examples



Shows how to use the hard drive instead of memory when saving a document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// When we save a document, various elements are temporarily stored in memory as the save operation is taking place.
// We can use this option to use a temporary folder in the local file system instead,
// which will reduce our application's memory overhead.
auto options = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
options->set_TempFolder(get_ArtifactsDir() + u"TempFiles");

// The specified temporary folder must exist in the local file system before the save operation.
System::IO::Directory::CreateDirectory_(options->get_TempFolder());

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.TempFolder.doc", options);

// The folder will persist with no residual contents from the load operation.
ASSERT_EQ(0, System::IO::Directory::GetFiles(options->get_TempFolder())->get_Length());
```

## See Also

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
