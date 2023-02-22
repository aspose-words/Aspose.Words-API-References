---
title: Document.VbaProject
second_title: Справочник по API Aspose.Words для .NET
description: Document свойство. Получает или задаетVbaProject .
type: docs
weight: 430
url: /ru/net/aspose.words/document/vbaproject/
---
## Document.VbaProject property

Получает или задает`VbaProject` .

```csharp
public VbaProject VbaProject { get; set; }
```

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

* class [VbaProject](../../../aspose.words.vba/vbaproject/)
* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


