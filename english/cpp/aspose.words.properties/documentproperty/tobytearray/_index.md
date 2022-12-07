---
title: ToByteArray
second_title: Aspose.Words for C++ API Reference
description: Returns the property value as byte array.
type: docs
weight: 131
url: /cpp/aspose.words.properties/documentproperty/tobytearray/
---
## DocumentProperty::ToByteArray method


Returns the property value as byte array.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Properties::DocumentProperty::ToByteArray()
```

## Remarks


Throws an exception if the property type is not [ByteArray](../../propertytype/).

## Examples



Shows how to add a thumbnail to a document that we save as an Epub. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// If we save a document, whose "Thumbnail" property contains image data that we added, as an Epub,
// a reader that opens that document may display the image before the first page.
SharedPtr<BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

ArrayPtr<uint8_t> thumbnailBytes = System::IO::File::ReadAllBytes(ImageDir + u"Logo.jpg");
properties->set_Thumbnail(thumbnailBytes);

doc->Save(ArtifactsDir + u"DocumentProperties.Thumbnail.epub");

// We can extract a document's thumbnail image and save it to the local file system.
SharedPtr<DocumentProperty> thumbnail = doc->get_BuiltInDocumentProperties()->idx_get(u"Thumbnail");
System::IO::File::WriteAllBytes(ArtifactsDir + u"DocumentProperties.Thumbnail.gif", thumbnail->ToByteArray());
```

## See Also

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words](../../../)
