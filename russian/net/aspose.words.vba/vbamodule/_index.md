---
title: VbaModule Class
linktitle: VbaModule
articleTitle: VbaModule
second_title: Aspose.Words для .NET
description: Откройте для себя мощь Aspose.Words.Vba.VbaModule для бесперебойного доступа к модулям вашего проекта VBA. Повысьте производительность и оптимизируйте автоматизацию документов!
type: docs
weight: 7400
url: /ru/net/aspose.words.vba/vbamodule/
---
## VbaModule class

Предоставляет доступ к модулю проекта VBA.

Чтобы узнать больше, посетите[Работа с макросами VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) документальная статья.

```csharp
public class VbaModule
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [VbaModule](vbamodule/)() | Создает пустой модуль. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Name](../../aspose.words.vba/vbamodule/name/) { get; set; } | Возвращает или задает имя модуля проекта VBA. |
| [SourceCode](../../aspose.words.vba/vbamodule/sourcecode/) { get; set; } | Получает или задает исходный код модуля проекта VBA. |
| [Type](../../aspose.words.vba/vbamodule/type/) { get; set; } | Указывает, является ли модуль процедурным модулем, модулем документа, модулем класса или модулем дизайнера. |

## Методы

| Имя | Описание |
| --- | --- |
| [Clone](../../aspose.words.vba/vbamodule/clone/)() | Выполняет копирование`VbaModule` . |

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

* пространство имен [Aspose.Words.Vba](../../aspose.words.vba/)
* сборка [Aspose.Words](../../)
