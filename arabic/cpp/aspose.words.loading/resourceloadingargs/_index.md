---
title: "فئة Aspose::Words::Loading::ResourceLoadingArgs"
linktitle: "ResourceLoadingArgs"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Loading::ResourceLoadingArgs. توفر بيانات لطريقة ResourceLoading() في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.loading/resourceloadingargs/
---
## ResourceLoadingArgs class


توفر بيانات لطريقة [ResourceLoading()](../iresourceloadingcallback/resourceloading/).

```cpp
class ResourceLoadingArgs : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_OriginalUri](./get_originaluri/)() const | عنوان URI الأصلي للمورد كما هو محدد في المستند المستورد. |
| [get_ResourceType](./get_resourcetype/)() const | نوع المورد. |
| [get_Uri](./get_uri/)() const | عنوان URI للمورد الذي يُستخدم للتنزيل إذا أرجعت [ResourceLoading()](../iresourceloadingcallback/resourceloading/) القيمة [Default](../resourceloadingaction/). في البداية يتم تعيينه إلى URI المطلق للمورد، لكن يمكن للمستخدم إعادة تعريفه إلى أي قيمة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Uri](./set_uri/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Loading::ResourceLoadingArgs::get_Uri](./get_uri/). |
| [SetData](./setdata/)(const System::ArrayPtr\<uint8_t\>\&) | يضبط البيانات التي يقدمها المستخدم للمورد والتي تُستخدم إذا أرجعت [ResourceLoading()](../iresourceloadingcallback/resourceloading/) القيمة [UserProvided](../resourceloadingaction/). |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
