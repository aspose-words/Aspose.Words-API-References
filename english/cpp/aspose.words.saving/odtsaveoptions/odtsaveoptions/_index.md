---
title: Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions constructor
linktitle: OdtSaveOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions constructor. Initializes a new instance of this class that can be used to save a document in the Odt format in C++.'
type: docs
weight: 2000
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
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## See Also

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
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
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Create a new OdtSaveOptions, and pass either "SaveFormat.Odt",
// or "SaveFormat.Ott" as the format to save the document in.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(saveFormat);
saveOptions->set_Password(u"@sposeEncrypted_1145");

System::String extensionString = Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat);

// If we open this document with an appropriate editor,
// it will prompt us for the password we specified in the SaveOptions object.
doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString, saveOptions);

System::SharedPtr<Aspose::Words::FileFormatInfo> docInfo = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString);

ASSERT_TRUE(docInfo->get_IsEncrypted());

// If we wish to open or edit this document again using Aspose.Words,
// we will have to provide a LoadOptions object with the correct password to the loading constructor.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString, System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"@sposeEncrypted_1145"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## OdtSaveOptions::OdtSaveOptions(const System::String\&) constructor


Initializes a new instance of this class that can be used to save a document in the [Odt](../../../aspose.words/saveformat/) format encrypted with a password.

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions(const System::String &password)
```

## See Also

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
