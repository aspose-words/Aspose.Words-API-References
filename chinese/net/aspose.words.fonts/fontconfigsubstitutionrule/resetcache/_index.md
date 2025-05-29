---
title: FontConfigSubstitutionRule.ResetCache
linktitle: ResetCache
articleTitle: ResetCache
second_title: Aspose.Words for .NET
description: 使用 FontConfigSubstitutionRule 的 ResetCache 方法优化您的字体管理。轻松清除字体配置结果，提升性能。
type: docs
weight: 30
url: /zh/net/aspose.words.fonts/fontconfigsubstitutionrule/resetcache/
---
## FontConfigSubstitutionRule.ResetCache method

重置 fontconfig 调用结果的缓存。

```csharp
public void ResetCache()
```

## 例子

显示与操作系统相关的字体配置替换。

```csharp
FontSettings fontSettings = new FontSettings();
FontConfigSubstitutionRule fontConfigSubstitution =
    fontSettings.SubstitutionSettings.FontConfigSubstitution;

bool isWindows = new[] {PlatformID.Win32NT, PlatformID.Win32S, PlatformID.Win32Windows, PlatformID.WinCE}
    .Any(p => Environment.OSVersion.Platform == p);

// FontConfigSubstitutionRule 对象在 Windows 和非 Windows 平台上的工作方式不同。
// 在 Windows 上，它不可用。
if (isWindows)
{
    Assert.False(fontConfigSubstitution.Enabled);
    Assert.False(fontConfigSubstitution.IsFontConfigAvailable());
}

bool isLinuxOrMac =
    new[] {PlatformID.Unix, PlatformID.MacOSX}.Any(p => Environment.OSVersion.Platform == p);

// 在 Linux/Mac 上，我们将可以访问它，并能够执行操作。
if (isLinuxOrMac)
{
    Assert.True(fontConfigSubstitution.Enabled);
    Assert.True(fontConfigSubstitution.IsFontConfigAvailable());

    fontConfigSubstitution.ResetCache();
}
```

### 也可以看看

* class [FontConfigSubstitutionRule](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
