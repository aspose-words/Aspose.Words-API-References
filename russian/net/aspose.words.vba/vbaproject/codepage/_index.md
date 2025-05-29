---
title: VbaProject.CodePage
linktitle: CodePage
articleTitle: CodePage
second_title: Aspose.Words для .NET
description: Узнайте, как управлять свойством VbaProject CodePage, чтобы оптимизировать настройки кодовой страницы вашего проекта VBA для повышения производительности и совместимости.
type: docs
weight: 20
url: /ru/net/aspose.words.vba/vbaproject/codepage/
---
## VbaProject.CodePage property

Возвращает или задает кодовую страницу проекта VBA.

```csharp
public int CodePage { get; set; }
```

## Примечания

Обратите внимание, что VBA — это функция до Unicode, и вам необходимо явно задать соответствующую кодовую страницу для сохранения региональных наборов символов.

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
