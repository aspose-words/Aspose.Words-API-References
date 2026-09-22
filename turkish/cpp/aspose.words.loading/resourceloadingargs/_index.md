---
title: "Aspose::Words::Loading::ResourceLoadingArgs sınıfı"
linktitle: "ResourceLoadingArgs"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::ResourceLoadingArgs sınıfı. C++'ta ResourceLoading() yöntemi için veri sağlar."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.loading/resourceloadingargs/
---
## ResourceLoadingArgs class


[ResourceLoading()](../iresourceloadingcallback/resourceloading/) yöntemi için veri sağlar.

```cpp
class ResourceLoadingArgs : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_OriginalUri](./get_originaluri/)() const | İçe aktarılan belgede belirtildiği gibi kaynağın orijinal URI'si. |
| [get_ResourceType](./get_resourcetype/)() const | Kaynağın türü. |
| [get_Uri](./get_uri/)() const | Eğer [ResourceLoading()](../iresourceloadingcallback/resourceloading/) [Default](../resourceloadingaction/) döndürürse, indirme için kullanılan kaynağın URI'si. Başlangıçta kaynağın mutlak URI'sine ayarlanır, ancak kullanıcı bunu herhangi bir değere yeniden tanımlayabilir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Uri](./set_uri/)(const System::String\&) | Ayarlayıcı: [Aspose::Words::Loading::ResourceLoadingArgs::get_Uri](./get_uri/). |
| [SetData](./setdata/)(const System::ArrayPtr\<uint8_t\>\&) | Eğer [ResourceLoading()](../iresourceloadingcallback/resourceloading/) [UserProvided](../resourceloadingaction/) döndürürse, kullanılan kaynağın kullanıcı tarafından sağlanan verilerini ayarlar. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
