---
title: Class VbaModuleCollection
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Vba.VbaModuleCollection сорт. Представляет наборVbaModule объекты.
type: docs
weight: 6250
url: /ru/net/aspose.words.vba/vbamodulecollection/
---
## VbaModuleCollection class

Представляет набор[`VbaModule`](../vbamodule/) объекты.

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

Показывает, как получить доступ к информации о проекте документа VBA.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");

// Проект VBA содержит набор модулей VBA.
VbaProject vbaProject = doc.VbaProject;
    ? $"Project name: {vbaProject.Name} signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n"
    : $"Project name: {vbaProject.Name} not signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n");

VbaModuleCollection vbaModules = doc.VbaProject.Modules; 

Assert.AreEqual(vbaModules.Count(), 3);

foreach (VbaModule module in vbaModules)
    Console.WriteLine($"Module name: {module.Name};\nModule code:\n{module.SourceCode}\n");

// Установить новый исходный код для модуля VBA. Вы можете получить доступ к модулям VBA в коллекции либо по индексу, либо по имени.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// Удалить модуль из коллекции.
vbaModules.Remove(vbaModules[2]);
```

### Смотрите также

* class [VbaModule](../vbamodule/)
* пространство имен [Aspose.Words.Vba](../../aspose.words.vba/)
* сборка [Aspose.Words](../../)


