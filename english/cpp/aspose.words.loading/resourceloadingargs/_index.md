---
title: Aspose::Words::Loading::ResourceLoadingArgs class
linktitle: ResourceLoadingArgs
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::ResourceLoadingArgs class. Provides data for the ResourceLoading() method in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.loading/resourceloadingargs/
---
## ResourceLoadingArgs class


Provides data for the [ResourceLoading()](../iresourceloadingcallback/resourceloading/) method.

```cpp
class ResourceLoadingArgs : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_OriginalUri](./get_originaluri/)() const | Original URI of the resource as specified in imported document. |
| [get_ResourceType](./get_resourcetype/)() const | Type of resource. |
| [get_Uri](./get_uri/)() const | URI of the resource which is used for downloading if [ResourceLoading()](../iresourceloadingcallback/resourceloading/) returns [Default](../resourceloadingaction/). Initially it's set to absolute URI of the resource, but user can redefine it to any value. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Uri](./set_uri/)(const System::String\&) | Setter for [Aspose::Words::Loading::ResourceLoadingArgs::get_Uri](./get_uri/). |
| [SetData](./setdata/)(const System::ArrayPtr\<uint8_t\>\&) | Sets user provided data of the resource which is used if [ResourceLoading()](../iresourceloadingcallback/resourceloading/) returns [UserProvided](../resourceloadingaction/). |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
