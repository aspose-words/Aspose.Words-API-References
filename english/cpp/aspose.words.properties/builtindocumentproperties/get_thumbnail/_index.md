---
title: Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail method
linktitle: get_Thumbnail
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail method. Gets or sets the thumbnail of the document in C++.'
type: docs
weight: 28000
url: /cpp/aspose.words.properties/builtindocumentproperties/get_thumbnail/
---
## BuiltInDocumentProperties::get_Thumbnail method


Gets or sets the thumbnail of the document.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail()
```

## Remarks


For now this property is used only when a document is being exported to ePub, it's not read from and written to other document formats.

Image of arbitrary format can be set to this property, but the format is checked during export.

Only gif, jpeg and png images can be used for ePub publication.

## Examples



Shows how to add a thumbnail to a document that we save as an Epub. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// If we save a document, whose "Thumbnail" property contains image data that we added, as an Epub,
// a reader that opens that document may display the image before the first page.
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

System::ArrayPtr<uint8_t> thumbnailBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");
properties->set_Thumbnail(thumbnailBytes);

doc->Save(get_ArtifactsDir() + u"DocumentProperties.Thumbnail.epub");

// We can extract a document's thumbnail image and save it to the local file system.
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> thumbnail = doc->get_BuiltInDocumentProperties()->idx_get(u"Thumbnail");
System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"DocumentProperties.Thumbnail.gif", thumbnail->ToByteArray());
```

## See Also

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
