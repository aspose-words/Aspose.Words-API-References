---
title: get_TempFolder
second_title: Aspose.Words for C++ API Reference
description: Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is null and no temporary files are used.
type: docs
weight: 183
url: /cpp/aspose.words.saving/saveoptions/get_tempfolder/
---
## SaveOptions::get_TempFolder method


Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is **null** and no temporary files are used.

```cpp
System::String Aspose::Words::Saving::SaveOptions::get_TempFolder() const
```

## Remarks


When Aspose.Words saves a document, it needs to create temporary internal structures. By default, these internal structures are created in memory and the memory usage spikes for a short period while the document is being saved. When saving is complete, the memory is freed and reclaimed by the garbage collector.

If you are saving a very large document (thousands of pages) and/or processing many documents at the same time, then the memory spike during saving can be significant enough to cause the system to throw [OutOfMemoryException](../). Specifying a temporary folder using [TempFolder](./) will cause Aspose.Words to keep the internal structures in temporary files instead of memory. It reduces the memory usage during saving, but will decrease the save performance.

The folder must exist and be writable, otherwise an exception will be thrown.

Aspose.Words automatically deletes all temporary files when saving is complete.

## Examples



Shows how to use the hard drive instead of memory when saving a document. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

// When we save a document, various elements are temporarily stored in memory as the save operation is taking place.
// We can use this option to use a temporary folder in the local file system instead,
// which will reduce our application's memory overhead.
auto options = MakeObject<DocSaveOptions>();
options->set_TempFolder(ArtifactsDir + u"TempFiles");

// The specified temporary folder must exist in the local file system before the save operation.
System::IO::Directory::CreateDirectory_(options->get_TempFolder());

doc->Save(ArtifactsDir + u"DocSaveOptions.TempFolder.doc", options);

// The folder will persist with no residual contents from the load operation.
ASSERT_EQ(0, System::IO::Directory::GetFiles(options->get_TempFolder())->get_Length());
```

## See Also

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
