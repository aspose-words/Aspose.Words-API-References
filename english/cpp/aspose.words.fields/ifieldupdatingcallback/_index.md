---
title: Aspose::Words::Fields::IFieldUpdatingCallback interface
linktitle: IFieldUpdatingCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::IFieldUpdatingCallback interface. Implement this interface if you want to have your own custom methods called during a field update in C++.'
type: docs
weight: 123000
url: /cpp/aspose.words.fields/ifieldupdatingcallback/
---
## IFieldUpdatingCallback interface


Implement this interface if you want to have your own custom methods called during a field update.

```cpp
class IFieldUpdatingCallback : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [FieldUpdated](./fieldupdated/)(System::SharedPtr\<Aspose::Words::Fields::Field\>) | A user defined method that is called just after a field is updated. |
| virtual [FieldUpdating](./fieldupdating/)(System::SharedPtr\<Aspose::Words::Fields::Field\>) | A user defined method that is called just before a field is updated. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
