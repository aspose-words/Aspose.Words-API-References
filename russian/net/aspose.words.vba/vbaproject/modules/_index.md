---
title: VbaProject.Modules
second_title: Справочник по API Aspose.Words для .NET
description: VbaProject свойство. Возвращает коллекцию модулей проекта VBA.
type: docs
weight: 40
url: /ru/net/aspose.words.vba/vbaproject/modules/
---
## VbaProject.Modules property

Возвращает коллекцию модулей проекта VBA.

```csharp
public VbaModuleCollection Modules { get; }
```

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

* class [VbaModuleCollection](../../vbamodulecollection/)
* class [VbaProject](../)
* пространство имен [Aspose.Words.Vba](../../vbaproject/)
* сборка [Aspose.Words](../../../)


