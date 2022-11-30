---
title: get_AlwaysCompressMetafiles
second_title: Aspose.Words for C++ API Reference
description: When false, small metafiles are not compressed for performance reason. Default value is true, all metafiles are compressed regardless of its size.
type: docs
weight: 14
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
auto doc = MakeObject<Document>(MyDir + u"Microsoft equation object.docx");

// When we save a document, smaller metafiles are not compressed for performance reasons.
// We can set a flag in a SaveOptions object to compress every metafile when saving.
// Some editors such as LibreOffice cannot read uncompressed metafiles.
auto saveOptions = MakeObject<DocSaveOptions>();
saveOptions->set_AlwaysCompressMetafiles(compressAllMetafiles);

doc->Save(ArtifactsDir + u"DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);

if (compressAllMetafiles)
{
    ASSERT_LT(10000, MakeObject<System::IO::FileInfo>(ArtifactsDir + u"DocSaveOptions.AlwaysCompressMetafiles.docx")->get_Length());
}
else
{
    ASSERT_GE(30000, MakeObject<System::IO::FileInfo>(ArtifactsDir + u"DocSaveOptions.AlwaysCompressMetafiles.docx")->get_Length());
}
```

## See Also

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
