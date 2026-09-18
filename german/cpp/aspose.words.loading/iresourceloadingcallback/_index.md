---
title: "Aspose::Words::Loading::IResourceLoadingCallback Schnittstelle"
linktitle: "IResourceLoadingCallback"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::IResourceLoadingCallback Schnittstelle. Implementieren Sie diese Schnittstelle, wenn Sie steuern möchten, wie Aspose.Words externe Ressourcen beim Importieren eines Dokuments und Einfügen von Bildern mit DocumentBuilder in C++ lädt."
type: docs
weight: 11000
url: /de/cpp/aspose.words.loading/iresourceloadingcallback/
---
## IResourceLoadingCallback interface


Implementieren Sie diese Schnittstelle, wenn Sie steuern möchten, wie Aspose.Words externe Ressourcen beim Importieren eines Dokuments und Einfügen von Bildern mit [DocumentBuilder](../../aspose.words/documentbuilder/) lädt.

```cpp
class IResourceLoadingCallback : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [ResourceLoading](./resourceloading/)(System::SharedPtr\<Aspose::Words::Loading::ResourceLoadingArgs\>) | Wird aufgerufen, wenn Aspose.Words eine externe Ressource lädt. |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
