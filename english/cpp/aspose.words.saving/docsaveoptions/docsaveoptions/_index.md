---
title: DocSaveOptions
second_title: Aspose.Words for C++ API Reference
description: Initializes a new instance of this class that can be used to save a document in the Doc format.
type: docs
weight: 1
url: /cpp/aspose.words.saving/docsaveoptions/docsaveoptions/
---
## DocSaveOptions::DocSaveOptions() constructor


Initializes a new instance of this class that can be used to save a document in the [Doc](../../../aspose.words/saveformat/) format.

```cpp
Aspose::Words::Saving::DocSaveOptions::DocSaveOptions()
```


## Examples



Shows how to set save options for older Microsoft Word formats. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto options = MakeObject<DocSaveOptions>(SaveFormat::Doc);

// Set a password which will protect the loading of the document by Microsoft Word or Aspose.Words.
// Note that this does not encrypt the contents of the document in any way.
options->set_Password(u"MyPassword");

// If the document contains a routing slip, we can preserve it while saving by setting this flag to true.
options->set_SaveRoutingSlip(true);

doc->Save(ArtifactsDir + u"DocSaveOptions.SaveAsDoc.doc", options);

// To be able to load the document,
// we will need to apply the password we specified in the DocSaveOptions object in a LoadOptions object.
ASSERT_THROW(doc = MakeObject<Document>(ArtifactsDir + u"DocSaveOptions.SaveAsDoc.doc"), IncorrectPasswordException);

auto loadOptions = MakeObject<LoadOptions>(u"MyPassword");
doc = MakeObject<Document>(ArtifactsDir + u"DocSaveOptions.SaveAsDoc.doc", loadOptions);

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## See Also

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
## DocSaveOptions::DocSaveOptions(Aspose::Words::SaveFormat) constructor


Initializes a new instance of this class that can be used to save a document in the [Doc](../../../aspose.words/saveformat/) or [Dot](../../../aspose.words/saveformat/) format.

```cpp
Aspose::Words::Saving::DocSaveOptions::DocSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Can be [Doc](../../../aspose.words/saveformat/) or [Dot](../../../aspose.words/saveformat/). |

## Examples



Shows how to set save options for older Microsoft Word formats. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto options = MakeObject<DocSaveOptions>(SaveFormat::Doc);

// Set a password which will protect the loading of the document by Microsoft Word or Aspose.Words.
// Note that this does not encrypt the contents of the document in any way.
options->set_Password(u"MyPassword");

// If the document contains a routing slip, we can preserve it while saving by setting this flag to true.
options->set_SaveRoutingSlip(true);

doc->Save(ArtifactsDir + u"DocSaveOptions.SaveAsDoc.doc", options);

// To be able to load the document,
// we will need to apply the password we specified in the DocSaveOptions object in a LoadOptions object.
ASSERT_THROW(doc = MakeObject<Document>(ArtifactsDir + u"DocSaveOptions.SaveAsDoc.doc"), IncorrectPasswordException);

auto loadOptions = MakeObject<LoadOptions>(u"MyPassword");
doc = MakeObject<Document>(ArtifactsDir + u"DocSaveOptions.SaveAsDoc.doc", loadOptions);

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
