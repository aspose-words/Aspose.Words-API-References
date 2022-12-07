---
title: IFieldUpdatingProgressCallback
second_title: Aspose.Words for C++ API Reference
description: Implement this interface if you want to track field updating progress.
type: docs
weight: 1600
url: /cpp/aspose.words.fields/ifieldupdatingprogresscallback/
---
## IFieldUpdatingProgressCallback interface


Implement this interface if you want to track field updating progress.

```cpp
class IFieldUpdatingProgressCallback : public System::Object
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
* Library [Aspose.Words](../../)
