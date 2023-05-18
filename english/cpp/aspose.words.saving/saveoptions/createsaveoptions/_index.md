---
title: Aspose::Words::Saving::SaveOptions::CreateSaveOptions method
linktitle: CreateSaveOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::SaveOptions::CreateSaveOptions method. Creates a save options object of a class suitable for the specified save format in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.saving/saveoptions/createsaveoptions/
---
## SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat) method


Creates a save options object of a class suitable for the specified save format.

```cpp
static System::SharedPtr<Aspose::Words::Saving::SaveOptions> Aspose::Words::Saving::SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | The save format for which to create a save options object. |

### ReturnValue

An object of a class that derives from [SaveOptions](../).

## Examples



Shows an option to optimize memory consumption when rendering large documents to PDF. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
SharedPtr<SaveOptions> saveOptions = SaveOptions::CreateSaveOptions(SaveFormat::Pdf);

// Set the "MemoryOptimization" property to "true" to lower the memory footprint of large documents' saving operations
// at the cost of increasing the duration of the operation.
// Set the "MemoryOptimization" property to "false" to save the document as a PDF normally.
saveOptions->set_MemoryOptimization(memoryOptimization);

doc->Save(ArtifactsDir + u"PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

## See Also

* Class [SaveOptions](../)
* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## SaveOptions::CreateSaveOptions(const System::String\&) method


Creates a save options object of a class suitable for the file extension specified in the given file name.

```cpp
static System::SharedPtr<Aspose::Words::Saving::SaveOptions> Aspose::Words::Saving::SaveOptions::CreateSaveOptions(const System::String &fileName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | The extension of this file name determines the class of the save options object to create. |

### ReturnValue

An object of a class that derives from [SaveOptions](../).

## Examples



Shows how to set a default template for documents that do not have attached templates. 
```cpp
auto doc = MakeObject<Document>();

// Enable automatic style updating, but do not attach a template document.
doc->set_AutomaticallyUpdateStyles(true);

ASSERT_EQ(String::Empty, doc->get_AttachedTemplate());

// Since there is no template document, the document had nowhere to track style changes.
// Use a SaveOptions object to automatically set a template
// if a document that we are saving does not have one.
SharedPtr<SaveOptions> options = SaveOptions::CreateSaveOptions(u"Document.DefaultTemplate.docx");
options->set_DefaultTemplate(MyDir + u"Business brochure.dotx");

doc->Save(ArtifactsDir + u"Document.DefaultTemplate.docx", options);
```

## See Also

* Class [SaveOptions](../)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
