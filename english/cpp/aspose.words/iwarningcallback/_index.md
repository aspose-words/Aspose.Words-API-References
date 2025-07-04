---
title: Aspose::Words::IWarningCallback interface
linktitle: IWarningCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::IWarningCallback interface. Implement this interface if you want to have your own custom method called to capture loss of fidelity warnings that can occur during document loading or saving in C++.'
type: docs
weight: 80000
url: /cpp/aspose.words/iwarningcallback/
---
## IWarningCallback interface


Implement this interface if you want to have your own custom method called to capture loss of fidelity warnings that can occur during document loading or saving.

```cpp
class IWarningCallback : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| virtual [Warning](./warning/)(System::SharedPtr\<Aspose::Words::WarningInfo\>) | Aspose.Words invokes this method when it encounters some issue during document loading or saving that might result in loss of formatting or data fidelity. |
## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
