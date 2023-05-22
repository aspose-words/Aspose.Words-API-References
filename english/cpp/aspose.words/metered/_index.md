---
title: Aspose::Words::Metered class
linktitle: Metered
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Metered class. Provides methods to set metered key. To learn more, visit the  documentation article in C++.'
type: docs
weight: 40000
url: /cpp/aspose.words/metered/
---
## Metered class


Provides methods to set metered key. To learn more, visit the [Licensing and Subscription](https://docs.aspose.com/words/cpp/licensing/) documentation article.

```cpp
class Metered : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| static [GetConsumptionCredit](./getconsumptioncredit/)() | Gets consumption credit. |
| static [GetConsumptionQuantity](./getconsumptionquantity/)() | Gets consumption file size. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Metered](./metered/)() | Initializes a new instance of this class. |
| [SetMeteredKey](./setmeteredkey/)(const System::String\&, const System::String\&) | Sets metered public and private key. If you purchase metered license, when start application, this API should be called, normally, this is enough. However, if always fail to upload consumption data and exceed 24 hours, the license will be set to evaluation status, to avoid such case, you should regularly check the license status, if it is evaluation status, call this API again. |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
