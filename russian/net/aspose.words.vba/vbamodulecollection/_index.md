---
title: Class VbaModuleCollection
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Vba.VbaModuleCollection сорт. Представляет коллекциюVbaModule объекты.
type: docs
weight: 6560
url: /ru/net/aspose.words.vba/vbamodulecollection/
---
## VbaModuleCollection class

Представляет коллекцию[`VbaModule`](../vbamodule/) объекты.

Чтобы узнать больше, посетите[Работа с макросами VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) статья документации.

```csharp
public sealed class VbaModuleCollection : IEnumerable<VbaModule>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.vba/vbamodulecollection/count/) { get; } | Возвращает количество модулей VBA в коллекции. |
| [Item](../../aspose.words.vba/vbamodulecollection/item/) { get; } | Получает[`VbaModule`](../vbamodule/) объект по индексу. (2 indexers) |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words.vba/vbamodulecollection/add/)(VbaModule) | Добавляет модуль в коллекцию. |
| [Remove](../../aspose.words.vba/vbamodulecollection/remove/)(VbaModule) | Удаляет указанный модуль из коллекции. |

### Примеры

Показывает, как получить доступ к информации о проекте VBA документа.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");

// Проект VBA содержит набор модулей VBA.
VbaProject vbaProject = doc.VbaProject;
Console.WriteLine(vbaProject.IsSigned
    ? $"Project name: {vbaProject.Name} signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n"
    : $"Project name: {vbaProject.Name} not signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n");

VbaModuleCollection vbaModules = doc.VbaProject.Modules; 

Assert.AreEqual(vbaModules.Count(), 3);

foreach (VbaModule module in vbaModules)
    Console.WriteLine($"Module name: {module.Name};\nModule code:\n{module.SourceCode}\n");

// Устанавливаем новый исходный код для модуля VBA. Доступ к модулям VBA в коллекции можно получить либо по индексу, либо по имени.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// Удалить модуль из коллекции.
vbaModules.Remove(vbaModules[2]);
```

### Смотрите также

* class [VbaModule](../vbamodule/)
* пространство имен [Aspose.Words.Vba](../../aspose.words.vba/)
* сборка [Aspose.Words](../../)


