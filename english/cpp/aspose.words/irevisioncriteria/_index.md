---
title: Aspose::Words::IRevisionCriteria interface
linktitle: IRevisionCriteria
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::IRevisionCriteria interface. Implement this interface if you want to control when certain Revision should be accepted/rejected or not by the Accept()/Reject() methods in C++.'
type: docs
weight: 79500
url: /cpp/aspose.words/irevisioncriteria/
---
## IRevisionCriteria interface


Implement this interface if you want to control when certain [Revision](../revision/) should be accepted/rejected or not by the [Accept()](../)/[Reject()](../) methods.

```cpp
class IRevisionCriteria : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [IsMatch](./ismatch/)(System::SharedPtr\<Aspose::Words::Revision\>) | Checks whether or not specified *revision* matches criteria. |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
