---
title: "Aspose::Words::Fields::IFieldUpdatingCallback interface"
linktitle: "IFieldUpdatingCallback"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::IFieldUpdatingCallback 接口。如果您希望在 C++ 中字段更新期间调用您自己的自定义方法，请实现此接口。"
type: docs
weight: 123000
url: /zh/cpp/aspose.words.fields/ifieldupdatingcallback/
---
## IFieldUpdatingCallback interface


如果您希望在字段更新期间调用自定义方法，请实现此接口。

```cpp
class IFieldUpdatingCallback : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [FieldUpdated](./fieldupdated/)(System::SharedPtr\<Aspose::Words::Fields::Field\>) | 在字段更新后立即调用的用户定义方法。 |
| virtual [FieldUpdating](./fieldupdating/)(System::SharedPtr\<Aspose::Words::Fields::Field\>) | 在字段更新前立即调用的用户定义方法。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
