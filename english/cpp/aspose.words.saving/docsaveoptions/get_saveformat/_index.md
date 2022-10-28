---
title: get_SaveFormat
second_title: Aspose.Words for C++ API Reference
description: Specifies the format in which the document will be saved if this save options object is used. Can be Doc or Dot.
type: docs
weight: 40
url: /cpp/aspose.words.saving/docsaveoptions/get_saveformat/
---
## DocSaveOptions.get_SaveFormat method


Specifies the format in which the document will be saved if this save options object is used. Can be **Doc** or **Dot**.

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::DocSaveOptions::get_SaveFormat() override
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

