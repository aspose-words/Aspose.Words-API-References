---
title: "Aspose::Words::Layout::IPageLayoutCallback Schnittstelle"
linktitle: "IPageLayoutCallback"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Layout::IPageLayoutCallback Schnittstelle. Implementieren Sie diese Schnittstelle, wenn Sie Ihre eigene benutzerdefinierte Methode haben möchten, die während des Aufbaus und der Darstellung des Seitenlayoutmodells in C++ aufgerufen wird."
type: docs
weight: 6000
url: /de/cpp/aspose.words.layout/ipagelayoutcallback/
---
## IPageLayoutCallback interface


Implementieren Sie dieses Interface, wenn Sie Ihre eigene benutzerdefinierte Methode haben möchten, die während des Aufbaus und der Renderung des Seitenlayoutmodells aufgerufen wird.

```cpp
class IPageLayoutCallback : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Layout::PageLayoutCallbackArgs\>) | Dies wird aufgerufen, um über den Fortschritt des Layoutaufbaus und der Darstellung zu informieren. |
| static [Type](./type/)() |  |
## Hinweise


Der Hauptzweck dieser Schnittstelle besteht darin, Anwendungscode das Abbrechen des Build‑Vorgangs zu ermöglichen.

Es ist möglich, das Seitenlayout‑Modell nur für einige wenige Seiten zu Beginn des Dokuments zu erstellen, dann den Vorgang abzubrechen und nur das bereits Erstellte zu rendern.

Beachten Sie jedoch, dass die Rendering‑Ergebnisse möglicherweise nicht dem entsprechen, was für jede Seite gerendert worden wäre, wenn der Vorgang abgeschlossen worden wäre.

Diese Technik funktioniert möglicherweise nicht für jedes Dokument oder kann vollständig fehlschlagen.

## Siehe auch

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
