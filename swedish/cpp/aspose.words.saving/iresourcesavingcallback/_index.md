---
title: "Aspose::Words::Saving::IResourceSavingCallback interface"
linktitle: "IResourceSavingCallback"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::IResourceSavingCallback interface. Implementera detta gränssnitt om du vill styra hur Aspose.Words sparar externa resurser (bilder, typsnitt och css) när ett dokument sparas till fast sid HTML eller SVG i C++."
type: docs
weight: 45000
url: /sv/cpp/aspose.words.saving/iresourcesavingcallback/
---
## IResourceSavingCallback interface


Implementera detta gränssnitt om du vill kontrollera hur Aspose.Words sparar externa resurser (bilder, teckensnitt och css) när ett dokument sparas till fast sid-HTML eller SVG.

```cpp
class IResourceSavingCallback : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [ResourceSaving](./resourcesaving/)(System::SharedPtr\<Aspose::Words::Saving::ResourceSavingArgs\>) | Kallas när Aspose.Words sparar en extern resurs till fasta sidformat HTML eller SVG. |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
