---
title: Aspose::Words::Replacing::IReplacingCallback interface
linktitle: IReplacingCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Replacing::IReplacingCallback interface. Implement this interface if you want to have your own custom method called during a find and replace operation in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.replacing/ireplacingcallback/
---
## IReplacingCallback interface


Implement this interface if you want to have your own custom method called during a find and replace operation.

```cpp
class IReplacingCallback : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Replacing](./replacing/)(System::SharedPtr\<Aspose::Words::Replacing::ReplacingArgs\>) | A user defined method that is called during a replace operation for each match found just before a replace is made. |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
