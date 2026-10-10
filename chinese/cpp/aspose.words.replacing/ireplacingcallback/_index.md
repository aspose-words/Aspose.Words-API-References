---
title: "Aspose::Words::Replacing::IReplacingCallback 接口"
linktitle: "IReplacingCallback"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Replacing::IReplacingCallback 接口。如果您希望在 C++ 中的查找和替换操作期间调用自定义方法，请实现此接口。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.replacing/ireplacingcallback/
---
## IReplacingCallback interface


如果希望在查找和替换操作期间调用自定义方法，请实现此接口。

```cpp
class IReplacingCallback : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Replacing](./replacing/)(System::SharedPtr\<Aspose::Words::Replacing::ReplacingArgs\>) | 在替换操作期间，对每个找到的匹配，在实际替换之前调用的用户自定义方法。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
