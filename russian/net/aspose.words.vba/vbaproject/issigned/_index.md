---
title: VbaProject.IsSigned
linktitle: IsSigned
articleTitle: IsSigned
second_title: Aspose.Words для .NET
description: Откройте для себя свойство VbaProject IsSigned, чтобы легко проверять подписи проектов и повышать безопасность кода. Убедитесь, что ваши проекты VBA надежны!
type: docs
weight: 40
url: /ru/net/aspose.words.vba/vbaproject/issigned/
---
## VbaProject.IsSigned property

Показывает, является ли[`VbaProject`](../) подписан или нет.

```csharp
public bool IsSigned { get; }
```

## Примеры

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

// Установить новый исходный код для модуля VBA. Вы можете получить доступ к модулям VBA в коллекции либо по индексу, либо по имени.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// Удалить модуль из коллекции.
vbaModules.Remove(vbaModules[2]);
```

### Смотрите также

* class [VbaProject](../)
* пространство имен [Aspose.Words.Vba](../../../aspose.words.vba/)
* сборка [Aspose.Words](../../../)
