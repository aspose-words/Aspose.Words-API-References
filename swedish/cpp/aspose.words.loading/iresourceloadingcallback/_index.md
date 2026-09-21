---
title: "Aspose::Words::Loading::IResourceLoadingCallback interface"
linktitle: "IResourceLoadingCallback"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::IResourceLoadingCallback interface. Implementera detta gränssnitt om du vill styra hur Aspose.Words laddar externa resurser när du importerar ett dokument och infogar bilder med DocumentBuilder i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words.loading/iresourceloadingcallback/
---
## IResourceLoadingCallback interface


Implementera detta gränssnitt om du vill styra hur Aspose.Words laddar externa resurser när du infogar bilder med [DocumentBuilder](../../aspose.words/documentbuilder/).

```cpp
class IResourceLoadingCallback : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [ResourceLoading](./resourceloading/)(System::SharedPtr\<Aspose::Words::Loading::ResourceLoadingArgs\>) | Kallas när Aspose.Words laddar någon extern resurs. |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
