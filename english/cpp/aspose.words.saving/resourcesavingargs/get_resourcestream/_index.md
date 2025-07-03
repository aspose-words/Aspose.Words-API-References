---
title: Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream method
linktitle: get_ResourceStream
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream method. Allows to specify the stream where the resource will be saved to in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.saving/resourcesavingargs/get_resourcestream/
---
## ResourceSavingArgs::get_ResourceStream method


Allows to specify the stream where the resource will be saved to.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream() const
```

## Remarks


This property allows you to save resources to streams instead of files.

The default value is **null**. When this property is **null**, the resource will be saved to a file specified in the [ResourceFileName](../get_resourcefilename/) property.

Using [IResourceSavingCallback](../../iresourcesavingcallback/) you cannot substitute one resource with another. It is intended only for control over location where to save resources.

## See Also

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
