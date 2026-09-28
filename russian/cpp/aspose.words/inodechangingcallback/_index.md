---
title: "Aspose::Words::INodeChangingCallback interface"
linktitle: "INodeChangingCallback"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::INodeChangingCallback interface. Реализуйте этот интерфейс, если хотите получать уведомления о вставке или удалении узлов в документе в C++."
type: docs
weight: 79000
url: /ru/cpp/aspose.words/inodechangingcallback/
---
## INodeChangingCallback interface


Реализуйте этот интерфейс, если хотите получать уведомления о вставке или удалении узлов в документе.

```cpp
class INodeChangingCallback : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [NodeInserted](./nodeinserted/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Вызывается, когда узел, принадлежащий этому документу, был вставлен в другой узел. |
| virtual [NodeInserting](./nodeinserting/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Вызывается непосредственно перед тем, как узел, принадлежащий этому документу, будет вставлен в другой узел. |
| virtual [NodeRemoved](./noderemoved/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Вызывается, когда узел, принадлежащий этому документу, был удалён из своего родителя. |
| virtual [NodeRemoving](./noderemoving/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Вызывается непосредственно перед тем, как узел, принадлежащий этому документу, будет удалён из документа. |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
