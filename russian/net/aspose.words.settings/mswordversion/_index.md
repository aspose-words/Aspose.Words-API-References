---
title: Enum MsWordVersion
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Settings.MsWordVersion перечисление. Позволяет Aspose.Wods имитировать поведение приложения MS Word зависящее от версии.
type: docs
weight: 5860
url: /ru/net/aspose.words.settings/mswordversion/
---
## MsWordVersion enumeration

Позволяет Aspose.Wods имитировать поведение приложения MS Word, зависящее от версии.

```csharp
public enum MsWordVersion
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Word2000 | `0` | Оптимизировать поведение Aspose.Words в соответствии с версией MS Word 2000. |
| Word2002 | `1` | Оптимизировать поведение Aspose.Words в соответствии с версией MS Word 2002. |
| Word2003 | `2` | Оптимизировать поведение Aspose.Words в соответствии с версией MS Word 2003. |
| Word2007 | `3` | Оптимизировать поведение Aspose.Words в соответствии с версией MS Word 2007. |
| Word2010 | `4` | Оптимизировать поведение Aspose.Words в соответствии с версией MS Word 2010. |
| Word2013 | `5` | Оптимизировать поведение Aspose.Words в соответствии с версией MS Word 2013. |
| Word2016 | `6` | Оптимизировать поведение Aspose.Words в соответствии с версией MS Word 2016. |
| Word2019 | `7` | Оптимизировать поведение Aspose.Words в соответствии с версией MS Word 2019. |

### Примеры

Показывает, как оптимизировать документ для разных версий Microsoft Word.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // Этот объект содержит обширный список флагов, уникальных для каждого документа
    // которые позволяют нам обеспечить обратную совместимость со старыми версиями Microsoft Word.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // Распечатываем настройки по умолчанию для пустого документа.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // Мы можем получить доступ к этим настройкам в Microsoft Word через «Файл» -> gt; «Параметры» -> «Дополнительно» -> «Параметры совместимости для...».
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // Мы можем использовать метод OptimizeFor, чтобы обеспечить оптимальную совместимость с конкретной версией Microsoft Word.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
/// Группирует все флаги в объекте параметров совместимости документа по состоянию, а затем печатает каждую группу.
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

* пространство имен [Aspose.Words.Settings](../../aspose.words.settings/)
* сборка [Aspose.Words](../../)


