---
title: Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName method
linktitle: get_OriginalFileName
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName method. The name of the CHM file. Default value is null in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.loading/chmloadoptions/get_originalfilename/
---
## ChmLoadOptions::get_OriginalFileName method


The name of the CHM file. Default value is **null**.

```cpp
System::String Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName() const
```

## Remarks


CHM documents may contain links that reference the same document by file name. Aspose.Words supports such links and normally uses [OriginalFileName](../../../aspose.words/document/get_originalfilename/) to check whether the file referenced by a link is the file that is being loaded. If a document is loaded from a stream, its original file name should be specified explicitly via this property, since it cannot be determined automatically.

If a CHM document is loaded from a file and a non-null value for this property is specified, the value will take priority over the actual name of the file stored in [OriginalFileName](../../../aspose.words/document/get_originalfilename/).

## Examples



Shows how to resolve URLs like "ms-its:myfile.chm::/index.htm". 
```cpp
// Our document contains URLs like "ms-its:amhelp.chm::....htm", but it has a different name,
// so file links don't work after saving it to HTML.
// We need to define the original filename in 'ChmLoadOptions' to avoid this behavior.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::ChmLoadOptions>();
loadOptions->set_OriginalFileName(u"amhelp.chm");

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::IO::File::ReadAllBytes(get_MyDir() + u"Document with ms-its links.chm")), loadOptions);

doc->Save(get_ArtifactsDir() + u"ExChmLoadOptions.OriginalFileName.html");
```

## See Also

* Class [ChmLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
