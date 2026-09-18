---
title: "Aspose::Words::INodeChangingCallback interface"
linktitle: "INodeChangingCallback"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::INodeChangingCallback interface. Implementieren Sie diese Schnittstelle, wenn Sie Benachrichtigungen erhalten möchten, wenn Knoten im Dokument in C++ eingefügt oder entfernt werden."
type: docs
weight: 79000
url: /de/cpp/aspose.words/inodechangingcallback/
---
## INodeChangingCallback interface


Implementieren Sie diese Schnittstelle, wenn Sie Benachrichtigungen erhalten möchten, wenn Knoten im Dokument eingefügt oder entfernt werden.

```cpp
class INodeChangingCallback : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [NodeInserted](./nodeinserted/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Wird aufgerufen, wenn ein zu diesem Dokument gehörender Knoten in einen anderen Knoten eingefügt wurde. |
| virtual [NodeInserting](./nodeinserting/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Wird unmittelbar bevor ein zu diesem Dokument gehörender Knoten in einen anderen Knoten eingefügt werden soll, aufgerufen. |
| virtual [NodeRemoved](./noderemoved/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Wird aufgerufen, wenn ein zu diesem Dokument gehörender Knoten aus seinem übergeordneten Knoten entfernt wurde. |
| virtual [NodeRemoving](./noderemoving/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Wird unmittelbar aufgerufen, bevor ein Knoten, der zu diesem Dokument gehört, aus dem Dokument entfernt werden soll. |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
