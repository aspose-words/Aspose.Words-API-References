---
title: "Aspose::Words::INodeChangingCallback interface"
linktitle: "INodeChangingCallback"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::INodeChangingCallback interface. نفّذ هذه الواجهة إذا كنت ترغب في تلقي إشعارات عندما يتم إدراج أو إزالة العقد في المستند في C++."
type: docs
weight: 79000
url: /ar/cpp/aspose.words/inodechangingcallback/
---
## INodeChangingCallback interface


نفّذ هذه الواجهة إذا كنت تريد تلقي إشعارات عندما يتم إدراج أو إزالة العقد في المستند.

```cpp
class INodeChangingCallback : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [NodeInserted](./nodeinserted/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | يُستدعى عندما يتم إدراج عقدة تابعة لهذا المستند في عقدة أخرى. |
| virtual [NodeInserting](./nodeinserting/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | يُستدعى قبل قليل عندما تكون عقدة تابعة لهذا المستند على وشك أن تُدرج في عقدة أخرى. |
| virtual [NodeRemoved](./noderemoved/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | يُستدعى عندما تُزيل عقدة تابعة لهذا المستند من الأصل. |
| virtual [NodeRemoving](./noderemoving/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | يُستدعى قبل قليل عندما تكون عقدة تابعة لهذا المستند على وشك أن تُزال من المستند. |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
