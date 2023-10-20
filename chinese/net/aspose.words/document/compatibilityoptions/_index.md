---
title: Document.CompatibilityOptions
linktitle: CompatibilityOptions
articleTitle: CompatibilityOptions
second_title: 用于 .NET 的 Aspose.Words
description: Document CompatibilityOptions 财产. 提供对文档兼容性选项的访问即在兼容性 选项卡选项Word 中的对话框 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words/document/compatibilityoptions/
---
## Document.CompatibilityOptions property

提供对文档兼容性选项的访问（即，在**兼容性** 选项卡**选项**Word 中的对话框）.

```csharp
public CompatibilityOptions CompatibilityOptions { get; }
```

## 例子

展示如何针对不同版本的 Microsoft Word 优化文档。

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // 此对象包含每个文档唯一的大量标志列表
    // 这使我们能够促进与旧版本的 Microsoft Word 的向后兼容性。
    CompatibilityOptions options = doc.CompatibilityOptions;

    // 打印空白文档的默认设置。
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // 我们可以在 Microsoft Word 中通过“文件”访问这些设置 -> “选项”-> “高级”-> “...的兼容性选项”。
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // 我们可以使用 OptimizeFor 方法来确保与特定 Microsoft Word 版本的最佳兼容性。
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
/// 按状态对文档的兼容性选项对象中的所有标志进行分组，然后打印每个组。
/// </summary>
private static void PrintCompatibilityOptions(CompatibilityOptions options)
{
    for (int i = 1; i >= 0; i--)
    {
        Console.WriteLine(Convert.ToBoolean(i) ? "\tEnabled options:" : "\tDisabled options:");
        SortedSet<string> optionNames = new SortedSet<string>();

        foreach (System.ComponentModel.PropertyDescriptor descriptor in System.ComponentModel.TypeDescriptor.GetProperties(options))
        {
            if (descriptor.PropertyType == Type.GetType("System.Boolean") && i == Convert.ToInt32(descriptor.GetValue(options)))
            {
                optionNames.Add(descriptor.Name);
            }
        }

        foreach (string s in optionNames)
        {
            Console.WriteLine($"\t\t{s}");
        }
    }
}
```

### 也可以看看

* class [CompatibilityOptions](../../../aspose.words.settings/compatibilityoptions/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
