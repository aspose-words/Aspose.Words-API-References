---
title: "Aspose::Words::License::SetLicense 方法"
linktitle: "SetLicense"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::License::SetLicense 方法。 在 C++ 中为组件授权。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words/license/setlicense/
---
## License::SetLicense(const System::SharedPtr\<System::IO::Stream\>\&) method


为组件授权。

```cpp
void Aspose::Words::License::SetLicense(const System::SharedPtr<System::IO::Stream> &stream)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 流 | const System::SharedPtr\<System::IO::Stream\>\& | 包含许可证的流。 |
## 备注


使用此方法从流中加载许可证。

## 示例



展示如何从流初始化 Aspose.Words 的许可证。
```cpp
System::String testLicenseFileName = u"Aspose.Words.Cpp.lic";
// 通过传入本地文件系统中有效许可证文件的流，为我们的 Aspose.Words 产品设置许可证。
{
    System::SharedPtr<System::IO::Stream> myStream = System::IO::File::OpenRead(System::IO::Path::Combine(get_LicenseDir(), testLicenseFileName));
    auto license = System::MakeObject<Aspose::Words::License>();
    license->SetLicense(myStream);
}
```

## 另见

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## License::SetLicense(const System::String\&) method


为组件授权。

```cpp
void Aspose::Words::License::SetLicense(const System::String &licenseName)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| licenseName | const System::String\& | 可以是完整或简短的文件名。使用空字符串切换到评估模式。 |
## 备注


尝试在以下位置查找许可证：

1. 明确路径。
1. 包含 Aspose.Words 库的文件夹。
1. 包含客户端应用程序的文件夹。



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

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## License::SetLicense(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::License::SetLicense(std::basic_istream<CharType, Traits> &stream)
```

## 另见

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
