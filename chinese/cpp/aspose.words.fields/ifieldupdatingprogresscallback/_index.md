---
title: "Aspose::Words::Fields::IFieldUpdatingProgressCallback 接口"
linktitle: "IFieldUpdatingProgressCallback"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::IFieldUpdatingProgressCallback 接口。如果您想在 C++ 中跟踪字段更新进度，请实现此接口。"
type: docs
weight: 124000
url: /zh/cpp/aspose.words.fields/ifieldupdatingprogresscallback/
---
## IFieldUpdatingProgressCallback interface


如果您想跟踪字段更新进度，请实现此接口。

```cpp
class IFieldUpdatingProgressCallback : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Fields::FieldUpdatingProgressArgs\>) | 当更新进度更改时调用的用户定义方法。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
