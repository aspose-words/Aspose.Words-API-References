---
title: "Aspose::Words::Loading::ResourceLoadingArgs 类"
linktitle: "ResourceLoadingArgs"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::ResourceLoadingArgs 类。提供 C++ 中 ResourceLoading() 方法的数据。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.loading/resourceloadingargs/
---
## ResourceLoadingArgs class


提供 [ResourceLoading()](../iresourceloadingcallback/resourceloading/) 方法的数据。

```cpp
class ResourceLoadingArgs : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_OriginalUri](./get_originaluri/)() const | 导入文档中指定的资源的原始 URI。 |
| [get_ResourceType](./get_resourcetype/)() const | 资源类型。 |
| [get_Uri](./get_uri/)() const | 如果 [ResourceLoading()](../iresourceloadingcallback/resourceloading/) 返回 [Default](../resourceloadingaction/)，则用于下载的资源 URI。最初它被设置为资源的绝对 URI，但用户可以将其重新定义为任意值。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Uri](./set_uri/)(const System::String\&) | 用于设置 [Aspose::Words::Loading::ResourceLoadingArgs::get_Uri](./get_uri/) 的 setter。 |
| [SetData](./setdata/)(const System::ArrayPtr\<uint8_t\>\&) | 如果 [ResourceLoading()](../iresourceloadingcallback/resourceloading/) 返回 [UserProvided](../resourceloadingaction/)，则设置资源的用户提供数据。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
