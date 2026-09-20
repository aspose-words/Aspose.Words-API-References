---
title: "Aspose::Words::INodeChangingCallback interfaz"
linktitle: "INodeChangingCallback"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::INodeChangingCallback interfaz. Implemente esta interfaz si desea recibir notificaciones cuando los nodos se insertan o eliminan en el documento en C++."
type: docs
weight: 79000
url: /es/cpp/aspose.words/inodechangingcallback/
---
## INodeChangingCallback interface


Implemente esta interfaz si desea recibir notificaciones cuando se inserten o eliminen nodos en el documento.

```cpp
class INodeChangingCallback : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [NodeInserted](./nodeinserted/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Se llama cuando un nodo perteneciente a este documento ha sido insertado en otro nodo. |
| virtual [NodeInserting](./nodeinserting/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Se llama justo antes de que un nodo perteneciente a este documento esté a punto de ser insertado en otro nodo. |
| virtual [NodeRemoved](./noderemoved/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Se llama cuando un nodo perteneciente a este documento ha sido eliminado de su padre. |
| virtual [NodeRemoving](./noderemoving/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Se llama justo antes de que un nodo perteneciente a este documento esté a punto de ser eliminado del documento. |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
