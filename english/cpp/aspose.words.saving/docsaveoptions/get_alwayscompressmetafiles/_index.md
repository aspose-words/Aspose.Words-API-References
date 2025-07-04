---
title: Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles method
linktitle: get_AlwaysCompressMetafiles
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles method. When false, small metafiles are not compressed for performance reason. Default value is true, all metafiles are compressed regardless of its size in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.saving/docsaveoptions/get_alwayscompressmetafiles/
---
## DocSaveOptions::get_AlwaysCompressMetafiles method


When **false**, small metafiles are not compressed for performance reason. Default value is **true**, all metafiles are compressed regardless of its size.

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles() const
```


## Examples



Shows how to change metafiles compression in a document while saving. 
```cpp
// Open a document that contains a Microsoft Equation 3.0 formula.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Microsoft equation object.docx");

// When we save a document, smaller metafiles are not compressed for performance reasons.
// We can set a flag in a SaveOptions object to compress every metafile when saving.
// Some editors such as LibreOffice cannot read uncompressed metafiles.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_AlwaysCompressMetafiles(compressAllMetafiles);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);
```

## See Also

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
