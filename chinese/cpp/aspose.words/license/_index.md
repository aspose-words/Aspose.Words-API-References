---
title: "Aspose::Words::License 类"
linktitle: "许可证"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::License 类。提供对组件进行授权的方法。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 39000
url: /zh/cpp/aspose.words/license/
---
## License class


提供对组件进行授权的方法。要了解更多，请访问 [Licensing and Subscription](https://docs.aspose.com/words/cpp/licensing/) 文档文章。

```cpp
class License : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [License](./license/)() | 初始化此类的新实例。 |
| [SetLicense](./setlicense/)(const System::String\&) | 为组件授权。 |
| [SetLicense](./setlicense/)(const System::SharedPtr\<System::IO::Stream\>\&) | 为组件授权。 |
| [SetLicense](./setlicense/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |

## 示例



展示如何使用本地文件系统中的许可证文件为 Aspose.Words 初始化许可证。
```cpp
System::String testLicenseFileName = u"Aspose.Words.Cpp.lic";

// 通过传递有效许可证文件的本地文件系统文件名，为我们的 Aspose.Words 产品设置许可证。
System::String licenseFileName = System::IO::Path::Combine(get_LicenseDir(), testLicenseFileName);

auto license = System::MakeObject<Aspose::Words::License>();
license->SetLicense(licenseFileName);

// 在我们应用程序的二进制文件夹中创建许可证文件的副本。
System::String licenseCopyFileName = System::IO::Path::Combine(get_AssemblyDir(), testLicenseFileName);
System::IO::File::Copy(licenseFileName, licenseCopyFileName);

// 如果我们传递的文件名没有路径，
// SetLicense 将在多个本地文件系统位置搜索此文件。
// 其中一个位置将是 "bin" 文件夹，其中包含我们的许可证文件副本。
license->SetLicense(testLicenseFileName);
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
