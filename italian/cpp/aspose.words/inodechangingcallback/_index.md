---
title: "Interfaccia Aspose::Words::INodeChangingCallback"
linktitle: "INodeChangingCallback"
second_title: "Riferimento API Aspose.Words per C++"
description: "Interfaccia Aspose::Words::INodeChangingCallback. Implementa questa interfaccia se desideri ricevere notifiche quando i nodi vengono inseriti o rimossi nel documento in C++."
type: docs
weight: 79000
url: /it/cpp/aspose.words/inodechangingcallback/
---
## INodeChangingCallback interface


Implementa questa interfaccia se desideri ricevere notifiche quando i nodi vengono inseriti o rimossi nel documento.

```cpp
class INodeChangingCallback : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [NodeInserted](./nodeinserted/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Chiamata quando un nodo appartenente a questo documento è stato inserito in un altro nodo. |
| virtual [NodeInserting](./nodeinserting/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Chiamata subito prima che un nodo appartenente a questo documento sia in procinto di essere inserito in un altro nodo. |
| virtual [NodeRemoved](./noderemoved/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Chiamata quando un nodo appartenente a questo documento è stato rimosso dal suo genitore. |
| virtual [NodeRemoving](./noderemoving/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Chiamata subito prima che un nodo appartenente a questo documento sia in procinto di essere rimosso dal documento. |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
