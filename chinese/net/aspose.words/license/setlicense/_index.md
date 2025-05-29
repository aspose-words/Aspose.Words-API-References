---
title: License.SetLicense
linktitle: SetLicense
articleTitle: SetLicense
second_title: Aspose.Words for .NET
description: 使用我们的 SetLicense 方法轻松授权您的组件。立即解锁全部功能，提升项目潜力！
type: docs
weight: 20
url: /zh/net/aspose.words/license/setlicense/
---
## SetLicense(*string*) {#setlicense_1}

许可组件。

```csharp
public void SetLicense(string licenseName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| licenseName | String | 可以是完整或短文件名或嵌入资源的名称。 使用空字符串切换到评估模式。 |

## 评论

尝试在以下位置查找许可证：

1.明确路径。

2. 包含 Aspose 组件程序集的文件夹。

3. 包含客户端调用程序集的文件夹。

4. 包含入口（启动）程序集的文件夹。

5. 客户端调用程序集中的嵌入资源。

**笔记：**在 .NET Compact Framework 上，尝试仅在以下位置查找许可证：

1.明确路径。

2. 客户端调用程序集中的嵌入资源。

## 例子

展示如何使用本地文件系统中的许可证文件初始化 Aspose.Words 的许可证。

```csharp
// 通过传递有效许可证文件的本地文件系统文件名来设置我们的 Aspose.Words 产品的许可证。
string licenseFileName = Path.Combine(LicenseDir, "Aspose.Words.NET.lic");

License license = new License();
license.SetLicense(licenseFileName);

// 在我们的应用程序的二进制文件夹中创建我们的许可证文件的副本。
string licenseCopyFileName = Path.Combine(AssemblyDir, "Aspose.Words.NET.lic");
File.Copy(licenseFileName, licenseCopyFileName);

// 如果我们传递一个没有路径的文件名，
// SetLicense 将在多个本地文件系统位置搜索该文件。
// 其中一个位置是“bin”文件夹，其中包含我们的许可证文件的副本。
license.SetLicense("Aspose.Words.NET.lic");
```

### 也可以看看

* class [License](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## SetLicense(*Stream*) {#setlicense}

许可组件。

```csharp
public void SetLicense(Stream stream)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 包含许可证的流。 |

## 评论

使用此方法从流中加载许可证。

## 例子

展示如何从流初始化 Aspose.Words 的许可证。

```csharp
// 通过在我们的本地文件系统中传递有效许可证文件流来设置我们的 Aspose.Words 产品的许可证。
using (Stream myStream = File.OpenRead(Path.Combine(LicenseDir, "Aspose.Words.NET.lic")))
{
    License license = new License();
    license.SetLicense(myStream);
}
```

### 也可以看看

* class [License](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
