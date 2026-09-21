---
title: "Aspose::Words::Loading::ResourceLoadingArgs klass"
linktitle: "ResourceLoadingArgs"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::ResourceLoadingArgs klass. Tillhandahåller data för metoden ResourceLoading() i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.loading/resourceloadingargs/
---
## ResourceLoadingArgs class


Tillhandahåller data för metoden [ResourceLoading()](../iresourceloadingcallback/resourceloading/).

```cpp
class ResourceLoadingArgs : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_OriginalUri](./get_originaluri/)() const | Ursprunglig URI för resursen som angivits i det importerade dokumentet. |
| [get_ResourceType](./get_resourcetype/)() const | Typ av resurs. |
| [get_Uri](./get_uri/)() const | URI för resursen som används för nedladdning om [ResourceLoading()](../iresourceloadingcallback/resourceloading/) returnerar [Default](../resourceloadingaction/). Initialt är den inställd på resursens absoluta URI, men användaren kan omdefiniera den till vilket värde som helst. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Uri](./set_uri/)(const System::String\&) | Sättare för [Aspose::Words::Loading::ResourceLoadingArgs::get_Uri](./get_uri/). |
| [SetData](./setdata/)(const System::ArrayPtr\<uint8_t\>\&) | Anger användarlevererad data för resursen som används om [ResourceLoading()](../iresourceloadingcallback/resourceloading/) returnerar [UserProvided](../resourceloadingaction/). |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
