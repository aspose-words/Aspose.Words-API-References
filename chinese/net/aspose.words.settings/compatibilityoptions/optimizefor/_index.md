---
title: OptimizeFor
second_title: Aspose.Words for .NET API 参考
description: 允许针对特定版本的 MS Word 优化文档内容以及默认 Aspose.Words 行为
type: docs
weight: 720
url: /zh/net/aspose.words.settings/compatibilityoptions/optimizefor/
---
## CompatibilityOptions.OptimizeFor method

允许针对特定版本的 MS Word 优化文档内容以及默认 Aspose.Words 行为。

使用此方法可防止 MS Word 在文档加载时显示“兼容模式”功能区。 （请注意，您可能还需要将[`Compliance`](../../../aspose.words.saving/ooxmlsaveoptions/compliance)属性设置为 Iso29500_2008_Transitional或更高。)

```csharp
public void OptimizeFor(MsWordVersion version)
```

### 例子

显示如何垂直对齐文本框的文本内容。

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

     // 这个对象包含一个广泛的标志列表，每个文档都是唯一的
     // 这使我们能够促进与旧版本的 Microsoft Word.
 的向后兼容性
    CompatibilityOptions options = doc.CompatibilityOptions;

    // 打印空白文档的默认设置。
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

     // 我们可以在 Microsoft Word 中通过“文件”访问这些设置 -> “选项”-> “高级”-> “...的兼容性选项”.
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

显示如何为保存的文档设置 OOXML 合规性规范以遵守。

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

     // 这个对象包含一个广泛的标志列表，每个文档都是唯一的
     // 这使我们能够促进与旧版本的 Microsoft Word.
 的向后兼容性
    CompatibilityOptions options = doc.CompatibilityOptions;

    // 打印空白文档的默认设置。
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

     // 我们可以在 Microsoft Word 中通过“文件”访问这些设置 -> “选项”-> “高级”-> “...的兼容性选项”.
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

展示如何针对不同版本的 Microsoft Word 优化文档。

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

     // 这个对象包含一个广泛的标志列表，每个文档都是唯一的
     // 这使我们能够促进与旧版本的 Microsoft Word.
 的向后兼容性
    CompatibilityOptions options = doc.CompatibilityOptions;

    // 打印空白文档的默认设置。
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

     // 我们可以在 Microsoft Word 中通过“文件”访问这些设置 -> “选项”-> “高级”-> “...的兼容性选项”.
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

* enum [MsWordVersion](../../mswordversion)
* class [CompatibilityOptions](../../compatibilityoptions)
* 命名空间 [Aspose.Words.Settings](../../compatibilityoptions)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
