---
title: Aspose::Words::Loading::LoadOptions::get_TempFolder method
linktitle: get_TempFolder
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::LoadOptions::get_TempFolder method. Allows to use temporary files when reading document. By default this property is null and no temporary files are used in C++.'
type: docs
weight: 16000
url: /cpp/aspose.words.loading/loadoptions/get_tempfolder/
---
## LoadOptions::get_TempFolder method


Allows to use temporary files when reading document. By default this property is **null** and no temporary files are used.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_TempFolder() const
```

## Remarks


The folder must exist and be writable, otherwise an exception will be thrown.

Aspose.Words automatically deletes all temporary files when reading is complete.

## Examples



Shows how to load a document using temporary files. 
```cpp
// Note that such an approach can reduce memory usage but degrades speed
auto loadOptions = MakeObject<LoadOptions>();
loadOptions->set_TempFolder(u"C:\\TempFolder\\");

// Ensure that the directory exists and load
System::IO::Directory::CreateDirectory_(loadOptions->get_TempFolder());

auto doc = MakeObject<Document>(MyDir + u"Document.docx", loadOptions);
```


Shows how to use the hard drive instead of memory when loading a document. 
```cpp
// When we load a document, various elements are temporarily stored in memory as the save operation occurs.
// We can use this option to use a temporary folder in the local file system instead,
// which will reduce our application's memory overhead.
auto options = MakeObject<LoadOptions>();
options->set_TempFolder(ArtifactsDir + u"TempFiles");

// The specified temporary folder must exist in the local file system before the load operation.
System::IO::Directory::CreateDirectory_(options->get_TempFolder());

auto doc = MakeObject<Document>(MyDir + u"Document.docx", options);

// The folder will persist with no residual contents from the load operation.
ASSERT_EQ(0, System::IO::Directory::GetFiles(options->get_TempFolder())->get_Length());
```

## See Also

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
