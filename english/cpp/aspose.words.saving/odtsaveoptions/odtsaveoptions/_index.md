---
title: OdtSaveOptions
second_title: Aspose.Words for C++ API Reference
description: Initializes a new instance of this class that can be used to save a document in the Odt format.
type: docs
weight: 1
url: /cpp/aspose.words.saving/odtsaveoptions/odtsaveoptions/
---
## OdtSaveOptions::OdtSaveOptions() constructor


Initializes a new instance of this class that can be used to save a document in the [Odt](../../../aspose.words/saveformat/) format.

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions()
```


## Examples



Shows how to make a saved document conform to an older ODT schema. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

auto saveOptions = MakeObject<OdtSaveOptions>();
saveOptions->set_MeasureUnit(OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(ArtifactsDir + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

## See Also

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
## OdtSaveOptions::OdtSaveOptions(Aspose::Words::SaveFormat) constructor


Initializes a new instance of this class that can be used to save a document in the [Odt](../../../aspose.words/saveformat/) or [Ott](../../../aspose.words/saveformat/) format.

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Can be [Odt](../../../aspose.words/saveformat/) or [Ott](../../../aspose.words/saveformat/). |

## Examples



Shows how to encrypt a saved ODT/OTT document with a password, and then load it using Aspose.Words. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Create a new OdtSaveOptions, and pass either "SaveFormat.Odt",
// or "SaveFormat.Ott" as the format to save the document in.
auto saveOptions = MakeObject<OdtSaveOptions>(saveFormat);
saveOptions->set_Password(u"@sposeEncrypted_1145");

String extensionString = FileFormatUtil::SaveFormatToExtension(saveFormat);

// If we open this document with an appropriate editor,
// it will prompt us for the password we specified in the SaveOptions object.
doc->Save(ArtifactsDir + u"OdtSaveOptions.Encrypt" + extensionString, saveOptions);

SharedPtr<FileFormatInfo> docInfo = FileFormatUtil::DetectFileFormat(ArtifactsDir + u"OdtSaveOptions.Encrypt" + extensionString);

ASSERT_TRUE(docInfo->get_IsEncrypted());

// If we wish to open or edit this document again using Aspose.Words,
// we will have to provide a LoadOptions object with the correct password to the loading constructor.
doc = MakeObject<Document>(ArtifactsDir + u"OdtSaveOptions.Encrypt" + extensionString, MakeObject<LoadOptions>(u"@sposeEncrypted_1145"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
## OdtSaveOptions::OdtSaveOptions(const System::String\&) constructor


Initializes a new instance of this class that can be used to save a document in the [Odt](../../../aspose.words/saveformat/) format encrypted with a password.

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions(const System::String &password)
```

## See Also

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
