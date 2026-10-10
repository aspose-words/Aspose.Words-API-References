---
title: "Interface Aspose::Words::INodeChangingCallback"
linktitle: "INodeChangingCallback"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Interface Aspose::Words::INodeChangingCallback. Implémentez cette interface si vous souhaitez recevoir des notifications lorsque des nœuds sont insérés ou supprimés dans le document en C++."
type: docs
weight: 79000
url: /fr/cpp/aspose.words/inodechangingcallback/
---
## INodeChangingCallback interface


Implémentez cette interface si vous souhaitez recevoir des notifications lorsque des nœuds sont insérés ou supprimés dans le document.

```cpp
class INodeChangingCallback : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [NodeInserted](./nodeinserted/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Appelé lorsqu'un nœud appartenant à ce document a été inséré dans un autre nœud. |
| virtual [NodeInserting](./nodeinserting/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Appelé juste avant qu'un nœud appartenant à ce document ne soit sur le point d'être inséré dans un autre nœud. |
| virtual [NodeRemoved](./noderemoved/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Appelé lorsqu'un nœud appartenant à ce document a été retiré de son parent. |
| virtual [NodeRemoving](./noderemoving/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Appelé juste avant qu'un nœud appartenant à ce document ne soit sur le point d'être retiré du document. |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
