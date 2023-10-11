---
title: Class License
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.License 班级. 提供组件许可方法
type: docs
weight: 3420
url: /zh/net/aspose.words/license/
---
## License class

提供组件许可方法。

要了解更多信息，请访问[许可和订阅](https://docs.aspose.com/words/net/licensing/)文档文章。

```csharp
public class License
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [License](license/)() | 初始化此类的新实例。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [SetLicense](../../aspose.words/license/setlicense/#setlicense)(Stream) | 许可组件。 |
| [SetLicense](../../aspose.words/license/setlicense/#setlicense_1)(string) | 许可组件。 |

### 例子

展示如何使用本地文件系统中的许可证文件初始化 Aspose.Words 许可证。

```csharp
// 通过传递有效许可证文件的本地文件系统文件名来设置 Aspose.Words 产品的许可证。
string licenseFileName = Path.Combine(LicenseDir, "Aspose.Words.NET.lic");

License license = new License();
license.SetLicense(licenseFileName);

// 在应用程序的二进制文件夹中创建许可证文件的副本。
string licenseCopyFileName = Path.Combine(AssemblyDir, "Aspose.Words.NET.lic");
File.Copy(licenseFileName, licenseCopyFileName);

// 如果我们传递一个不带路径的文件名，
// SetLicense 将在多个本地文件系统位置中搜索该文件。
// 这些位置之一是“bin”文件夹，其中包含我们的许可证文件的副本。
license.SetLicense("Aspose.Words.NET.lic");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)


