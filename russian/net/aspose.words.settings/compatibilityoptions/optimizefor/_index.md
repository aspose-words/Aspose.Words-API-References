---
title: OptimizeFor
second_title: Справочник по API Aspose.Words для .NET
description: Позволяет оптимизировать содержимое документа а также поведение Aspose.Words по умолчанию для определенных версий MS Word.
type: docs
weight: 720
url: /ru/net/aspose.words.settings/compatibilityoptions/optimizefor/
---
## CompatibilityOptions.OptimizeFor method

Позволяет оптимизировать содержимое документа, а также поведение Aspose.Words по умолчанию для определенных версий MS Word.

Используйте этот метод, чтобы MS Word не отображал ленту «Режим совместимости» при загрузке документа. (Обратите внимание, что вам также может понадобиться установить для свойства[`Compliance`](../../../aspose.words.saving/ooxmlsaveoptions/compliance)значение Iso29500_2008_Transitionalили выше.)

```csharp
public void OptimizeFor(MsWordVersion version)
```

### Примеры

Показывает как вертикально выровнять текстовое содержимое текстового поля.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

     // Этот объект содержит обширный список флагов, уникальных для каждого document
     // это позволяет нам обеспечить обратную совместимость со старыми версиями Microsoft Word.
    CompatibilityOptions options = doc.CompatibilityOptions;

     // Печать настроек по умолчанию для пустого документа.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

     // Мы можем получить доступ к этим настройкам в Microsoft Word через «Файл» -> "Опции" -> «Дополнительно» -> "Параметры совместимости для...".
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

     // Мы можем использовать метод OptimizeFor для обеспечения оптимальной совместимости с определенной версией Microsoft Word.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
 /// Группирует все флаги в объекте параметров совместимости документа по состоянию, затем печатает каждую группу.
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

Показывает, как установить спецификацию соответствия OOXML для сохраненного документа.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

     // Этот объект содержит обширный список флагов, уникальных для каждого document
     // это позволяет нам обеспечить обратную совместимость со старыми версиями Microsoft Word.
    CompatibilityOptions options = doc.CompatibilityOptions;

     // Печать настроек по умолчанию для пустого документа.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

     // Мы можем получить доступ к этим настройкам в Microsoft Word через «Файл» -> "Опции" -> «Дополнительно» -> "Параметры совместимости для...".
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

     // Мы можем использовать метод OptimizeFor для обеспечения оптимальной совместимости с определенной версией Microsoft Word.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
 /// Группирует все флаги в объекте параметров совместимости документа по состоянию, затем печатает каждую группу.
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

Показывает, как оптимизировать документ для различных версий Microsoft Word.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

     // Этот объект содержит обширный список флагов, уникальных для каждого document
     // это позволяет нам обеспечить обратную совместимость со старыми версиями Microsoft Word.
    CompatibilityOptions options = doc.CompatibilityOptions;

     // Печать настроек по умолчанию для пустого документа.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

     // Мы можем получить доступ к этим настройкам в Microsoft Word через «Файл» -> "Опции" -> «Дополнительно» -> "Параметры совместимости для...".
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

     // Мы можем использовать метод OptimizeFor для обеспечения оптимальной совместимости с определенной версией Microsoft Word.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
 /// Группирует все флаги в объекте параметров совместимости документа по состоянию, затем печатает каждую группу.
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

### Смотрите также

* enum [MsWordVersion](../../mswordversion)
* class [CompatibilityOptions](../../compatibilityoptions)
* пространство имен [Aspose.Words.Settings](../../compatibilityoptions)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
