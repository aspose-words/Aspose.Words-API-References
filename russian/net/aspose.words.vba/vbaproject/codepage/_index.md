---
title: VbaProject.CodePage
linktitle: CodePage
articleTitle: CodePage
second_title: Aspose.Words для .NET
description: VbaProject CodePage свойство. Получает или задает кодовую страницу проекта VBA на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.vba/vbaproject/codepage/
---
## VbaProject.CodePage property

Получает или задает кодовую страницу проекта VBA.

```csharp
public int CodePage { get; set; }
```

## Примечания

Обратите внимание, что VBA является функцией, предшествующей Unicode, и вам необходимо явно установить соответствующую кодовую страницу , чтобы сохранить региональные наборы символов.

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

// Устанавливаем новый исходный код для модуля VBA. Доступ к модулям VBA в коллекции можно получить либо по индексу, либо по имени.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// Удалить модуль из коллекции.
vbaModules.Remove(vbaModules[2]);
```

### Смотрите также

* class [VbaProject](../)
* пространство имен [Aspose.Words.Vba](../../../aspose.words.vba/)
* сборка [Aspose.Words](../../../)
