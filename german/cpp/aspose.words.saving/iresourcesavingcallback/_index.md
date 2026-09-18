---
title: "Aspose::Words::Saving::IResourceSavingCallback interface"
linktitle: "IResourceSavingCallback"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::IResourceSavingCallback interface. Implementieren Sie diese Schnittstelle, wenn Sie steuern möchten, wie Aspose.Words externe Ressourcen (Bilder, Schriftarten und CSS) beim Speichern eines Dokuments als festes Seiten‑HTML oder SVG in C++ speichert."
type: docs
weight: 45000
url: /de/cpp/aspose.words.saving/iresourcesavingcallback/
---
## IResourceSavingCallback interface


Implementieren Sie dieses Interface, wenn Sie steuern möchten, wie Aspose.Words externe Ressourcen (Bilder, Schriftarten und CSS) speichert, wenn ein Dokument als festes Seiten‑HTML oder SVG gespeichert wird.

```cpp
class IResourceSavingCallback : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [ResourceSaving](./resourcesaving/)(System::SharedPtr\<Aspose::Words::Saving::ResourceSavingArgs\>) | Wird aufgerufen, wenn Aspose.Words eine externe Ressource in das feste Seiten‑HTML‑ oder SVG‑Format speichert. |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
