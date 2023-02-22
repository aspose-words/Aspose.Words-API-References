---
title: Enum MsWordVersion
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Settings.MsWordVersion перечисление. Позволяет Aspose.Wods имитировать поведение приложения в зависимости от версии MS Word.
type: docs
weight: 5560
url: /ru/net/aspose.words.settings/mswordversion/
---
## MsWordVersion enumeration

Позволяет Aspose.Wods имитировать поведение приложения в зависимости от версии MS Word.

```csharp
public enum MsWordVersion
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Word2000 | `0` | Оптимизация поведения Aspose.Words в соответствии с версией MS Word 2000. |
| Word2002 | `1` | Оптимизация поведения Aspose.Words в соответствии с версией MS Word 2002. |
| Word2003 | `2` | Оптимизация поведения Aspose.Words в соответствии с версией MS Word 2003. |
| Word2007 | `3` | Оптимизация поведения Aspose.Words в соответствии с версией MS Word 2007. |
| Word2010 | `4` | Оптимизация поведения Aspose.Words в соответствии с версией MS Word 2010. |
| Word2013 | `5` | Оптимизация поведения Aspose.Words в соответствии с версией MS Word 2013. |
| Word2016 | `6` | Оптимизация поведения Aspose.Words в соответствии с версией MS Word 2016. |
| Word2019 | `7` | Оптимизировать поведение Aspose.Words, чтобы оно соответствовало версии MS Word 2019. |

### Примеры

Показывает, как оптимизировать документ для разных версий Microsoft Word.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // Этот объект содержит обширный список флагов, уникальных для каждого документа
    // которые позволяют нам обеспечить обратную совместимость со старыми версиями Microsoft Word.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // Печать настроек по умолчанию для пустого документа.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // Мы можем получить доступ к этим настройкам в Microsoft Word через «Файл» -> "Опции" -> «Дополнительно» -> "Параметры совместимости для...".
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // Мы можем использовать метод OptimizeFor, чтобы обеспечить оптимальную совместимость с определенной версией Microsoft Word.
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


