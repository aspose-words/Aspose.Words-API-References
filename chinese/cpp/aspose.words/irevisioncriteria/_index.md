---
title: "Aspose::Words::IRevisionCriteria 接口"
linktitle: "IRevisionCriteria"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::IRevisionCriteria 接口。如果您想通过 C++ 中的 Accept()/Reject() 方法控制何时接受/拒绝特定的 Revision，请实现此接口。"
type: docs
weight: 79500
url: /zh/cpp/aspose.words/irevisioncriteria/
---
## IRevisionCriteria interface


如果您想通过 [Accept()](../)/[Reject()](../) 方法控制何时接受/拒绝特定的 [Revision](../revision/)，请实现此接口。

```cpp
class IRevisionCriteria : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [IsMatch](./ismatch/)(System::SharedPtr\<Aspose::Words::Revision\>) | 检查指定的 *revision* 是否符合条件。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
