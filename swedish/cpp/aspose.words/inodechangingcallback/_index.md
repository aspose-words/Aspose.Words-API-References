---
title: "Aspose::Words::INodeChangingCallback interface"
linktitle: "INodeChangingCallback"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::INodeChangingCallback interface. Implementera detta gränssnitt om du vill få meddelanden när noder infogas eller tas bort i dokumentet i C++."
type: docs
weight: 79000
url: /sv/cpp/aspose.words/inodechangingcallback/
---
## INodeChangingCallback interface


Implementera detta gränssnitt om du vill få aviseringar när noder infogas eller tas bort i dokumentet.

```cpp
class INodeChangingCallback : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [NodeInserted](./nodeinserted/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Kallas när en nod som tillhör detta dokument har infogats i en annan nod. |
| virtual [NodeInserting](./nodeinserting/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Kallas precis innan en nod som tillhör detta dokument ska infogas i en annan nod. |
| virtual [NodeRemoved](./noderemoved/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Kallas när en nod som tillhör detta dokument har tagits bort från sin förälder. |
| virtual [NodeRemoving](./noderemoving/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Kallas precis innan en nod som tillhör detta dokument är på väg att tas bort från dokumentet. |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
