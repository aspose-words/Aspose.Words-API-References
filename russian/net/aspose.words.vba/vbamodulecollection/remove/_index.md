---
title: VbaModuleCollection.Remove
second_title: Справочник по API Aspose.Words для .NET
description: VbaModuleCollection метод. Удаляет указанный модуль из коллекции.
type: docs
weight: 40
url: /ru/net/aspose.words.vba/vbamodulecollection/remove/
---
## VbaModuleCollection.Remove method

Удаляет указанный модуль из коллекции.

```csharp
public void Remove(VbaModule module)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| module | VbaModule | Модуль, который нужно удалить. |

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

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* пространство имен [Aspose.Words.Vba](../../vbamodulecollection/)
* сборка [Aspose.Words](../../../)


