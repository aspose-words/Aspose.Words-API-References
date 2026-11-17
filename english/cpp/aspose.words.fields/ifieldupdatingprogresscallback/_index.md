---
title: Aspose::Words::Fields::IFieldUpdatingProgressCallback interface
linktitle: IFieldUpdatingProgressCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::IFieldUpdatingProgressCallback interface. Implement this interface if you want to track field updating progress in C++.'
type: docs
weight: 124000
url: /cpp/aspose.words.fields/ifieldupdatingprogresscallback/
---
## IFieldUpdatingProgressCallback interface


Implement this interface if you want to track field updating progress.

```cpp
class IFieldUpdatingProgressCallback : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Fields::FieldUpdatingProgressArgs\>) | A user defined method that is called when updating progress is changed. |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
