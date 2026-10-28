---
title: Aspose::Words::Saving::ResourceSavingArgs::set_ResourceStream method
linktitle: set_ResourceStream
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ResourceSavingArgs::set_ResourceStream method. Allows to specify the stream where the resource will be saved to in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words.saving/resourcesavingargs/set_resourcestream/
---
## ResourceSavingArgs::set_ResourceStream(const System::SharedPtr\<System::IO::Stream\> \&) method


Allows to specify the stream where the resource will be saved to.

```cpp
void Aspose::Words::Saving::ResourceSavingArgs::set_ResourceStream(const System::SharedPtr<System::IO::Stream> & value)
```

## Remarks


This property allows you to save resources to streams instead of files.

The default value is **null**. When this property is **null**, the resource will be saved to a file specified in the [ResourceFileName](../get_resourcefilename/) property.

Using [IResourceSavingCallback](../../iresourcesavingcallback/) you cannot substitute one resource with another. It is intended only for control over location where to save resources.
## See Also

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## ResourceSavingArgs::set_ResourceStream(std::basic_ostream\<CharType, Traits\> \&) method


Allows to specify the stream where the resource will be saved to.

```cpp
template<typename CharType,typename Traits> void Aspose::Words::Saving::ResourceSavingArgs::set_ResourceStream(std::basic_ostream<CharType, Traits> & value)
```

## Remarks


This property allows you to save resources to streams instead of files.

The default value is **null**. When this property is **null**, the resource will be saved to a file specified in the [ResourceFileName](../get_resourcefilename/) property.

Using [IResourceSavingCallback](../../iresourcesavingcallback/) you cannot substitute one resource with another. It is intended only for control over location where to save resources.
## See Also

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
