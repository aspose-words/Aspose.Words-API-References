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


Implement this interface if you want to control when certain [Revision](../revision/) should be accepted/rejected or not by the [Accept()](../revisioncollection/accept/)/[Reject()](../revisioncollection/reject/) methods.

```cpp
class IRevisionCriteria : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [IsMatch](./ismatch/)(System::SharedPtr\<Aspose::Words::Revision\>) | Checks whether or not specified revision matches criteria. |
## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
