---
title: TableSubstitutionRule.Save
linktitle: Save
articleTitle: Save
second_title: 用于 .NET 的 Aspose.Words
description: TableSubstitutionRule Save 方法. 将当前表替换设置保存到文件 在 C#.
type: docs
weight: 70
url: /zh/net/aspose.words.fonts/tablesubstitutionrule/save/
---
## Save(*string*) {#save_1}

将当前表替换设置保存到文件。

```csharp
public void Save(string fileName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 输出文件名。 |

## 例子

显示如何访问 Windows 和 Linux 的字体替换表。

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// 创建新的表替换规则并加载默认的 Microsoft Windows 字体替换表。
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// 在 Windows 中，“Times New Roman CE”字体的默认替代品是“Times New Roman”。
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// 我们可以将表格保存为 XML 文档的形式。
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

// Linux 有自己的替换表。
// “Times New Roman CE”有多种替代字体。
// 如果第一个替换，“FreeSerif”也不可用，
// 此规则将循环遍历数组中的其他规则，直到找到可用的规则。
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// 使用流以 XML 文档的形式保存 Linux 替换表。
using (FileStream fileStream = new FileStream(ArtifactsDir + "FontSettings.TableSubstitutionRule.Linux.xml",
    FileMode.Create))
{
    tableSubstitutionRule.Save(fileStream);
}
```

### 也可以看看

* class [TableSubstitutionRule](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)

---

## Save(*Stream*) {#save}

将当前表替换设置保存到流中。

```csharp
public void Save(Stream outputStream)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| outputStream | Stream | 输出流。 |

## 例子

显示如何访问 Windows 和 Linux 的字体替换表。

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// 创建新的表替换规则并加载默认的 Microsoft Windows 字体替换表。
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// 在 Windows 中，“Times New Roman CE”字体的默认替代品是“Times New Roman”。
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// 我们可以将表格保存为 XML 文档的形式。
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

// Linux 有自己的替换表。
// “Times New Roman CE”有多种替代字体。
// 如果第一个替换，“FreeSerif”也不可用，
// 此规则将循环遍历数组中的其他规则，直到找到可用的规则。
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// 使用流以 XML 文档的形式保存 Linux 替换表。
using (FileStream fileStream = new FileStream(ArtifactsDir + "FontSettings.TableSubstitutionRule.Linux.xml",
    FileMode.Create))
{
    tableSubstitutionRule.Save(fileStream);
}
```

### 也可以看看

* class [TableSubstitutionRule](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
