---
title: "Aspose::Words::Fields::IFieldUpdateCultureProvider 接口"
linktitle: "IFieldUpdateCultureProvider"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::IFieldUpdateCultureProvider 接口。实现后，提供一个在 C++ 中更新特定字段时应使用的 CultureInfo 对象。"
type: docs
weight: 122000
url: /zh/cpp/aspose.words.fields/ifieldupdatecultureprovider/
---
## IFieldUpdateCultureProvider interface


实现后，提供一个应在特定字段更新期间使用的 **CultureInfo** 对象。

```cpp
class IFieldUpdateCultureProvider : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [GetCulture](./getculture/)(System::String, System::SharedPtr\<Aspose::Words::Fields::Field\>) | 返回一个用于字段更新期间的 **CultureInfo** 对象。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
