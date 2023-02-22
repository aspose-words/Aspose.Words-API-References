---
title: Class FontSubstitutionRule
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Fonts.FontSubstitutionRule 班级. 这是字体替换规则的抽象基类
type: docs
weight: 2820
url: /zh/net/aspose.words.fonts/fontsubstitutionrule/
---
## FontSubstitutionRule class

这是字体替换规则的抽象基类。

```csharp
public abstract class FontSubstitutionRule
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | 指定是否启用规则。 |

### 例子

显示与操作系统相关的字体配置替换。

```csharp
FontSettings fontSettings = new FontSettings();
FontConfigSubstitutionRule fontConfigSubstitution =
    fontSettings.SubstitutionSettings.FontConfigSubstitution;

bool isWindows = new[] {PlatformID.Win32NT, PlatformID.Win32S, PlatformID.Win32Windows, PlatformID.WinCE}
    .Any(p => Environment.OSVersion.Platform == p);

// FontConfigSubstitutionRule 对象在 Windows/非 Windows 平台上的工作方式不同。
// 在 Windows 上，它不可用。
if (isWindows)
{
    Assert.False(fontConfigSubstitution.Enabled);
    Assert.False(fontConfigSubstitution.IsFontConfigAvailable());
}

bool isLinuxOrMac =
    new[] {PlatformID.Unix, PlatformID.MacOSX}.Any(p => Environment.OSVersion.Platform == p);

// 在 Linux/Mac 上，我们可以访问它，并且能够执行操作。
if (isLinuxOrMac)
{
    Assert.True(fontConfigSubstitution.Enabled);
    Assert.True(fontConfigSubstitution.IsFontConfigAvailable());

    fontConfigSubstitution.ResetCache();
}
```

### 也可以看看

* 命名空间 [Aspose.Words.Fonts](../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../)


