---
title: Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions constructor
linktitle: ChmLoadOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions constructor. Initializes a new instance of this class with default values in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.loading/chmloadoptions/chmloadoptions/
---
## ChmLoadOptions::ChmLoadOptions constructor


Initializes a new instance of this class with default values.

```cpp
Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions()
```


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
