---
title: "Aspose::Words::Replacing::IReplacingCallback Schnittstelle"
linktitle: "IReplacingCallback"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Replacing::IReplacingCallback‑Schnittstelle. Implementieren Sie diese Schnittstelle, wenn Sie Ihre eigene benutzerdefinierte Methode haben möchten, die während einer Suchen‑und‑Ersetzen‑Operation in C++ aufgerufen wird."
type: docs
weight: 3000
url: /de/cpp/aspose.words.replacing/ireplacingcallback/
---
## IReplacingCallback interface


Implementieren Sie dieses Interface, wenn Sie Ihre eigene benutzerdefinierte Methode während einer Suchen‑Ersetzen‑Operation aufrufen möchten.

```cpp
class IReplacingCallback : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Replacing](./replacing/)(System::SharedPtr\<Aspose::Words::Replacing::ReplacingArgs\>) | Eine benutzerdefinierte Methode, die während einer Ersetzungsoperation für jedes gefundene Treffer aufgerufen wird, unmittelbar bevor das Ersetzen durchgeführt wird. |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
