---
title: VbaProject Class
linktitle: VbaProject
articleTitle: VbaProject
second_title: Aspose.Words для .NET
description: Откройте для себя мощь класса Aspose.Words.Vba.VbaProject, чтобы без усилий управлять информацией и модулями проекта VBA в ваших документах. Улучшите свою автоматизацию сегодня!
type: docs
weight: 7430
url: /ru/net/aspose.words.vba/vbaproject/
---
## VbaProject class

Предоставляет доступ к информации о проекте VBA. Проект VBA внутри документа определяется как набор модулей VBA.

Чтобы узнать больше, посетите[Работа с макросами VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) документальная статья.

```csharp
public class VbaProject
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [VbaProject](vbaproject/)() | Создает пустое место`VbaProject` . |

## Характеристики

| Имя | Описание |
| --- | --- |
| [CodePage](../../aspose.words.vba/vbaproject/codepage/) { get; set; } | Возвращает или задает кодовую страницу проекта VBA. |
| [IsProtected](../../aspose.words.vba/vbaproject/isprotected/) { get; } | Показывает, является ли`VbaProject` защищен паролем. |
| [IsSigned](../../aspose.words.vba/vbaproject/issigned/) { get; } | Показывает, является ли`VbaProject` подписан или нет. |
| [Modules](../../aspose.words.vba/vbaproject/modules/) { get; } | Возвращает коллекцию модулей проекта VBA. |
| [Name](../../aspose.words.vba/vbaproject/name/) { get; set; } | Возвращает или задает имя проекта VBA. |
| [References](../../aspose.words.vba/vbaproject/references/) { get; } | Получает коллекцию ссылок на проекты VBA. |

## Методы

| Имя | Описание |
| --- | --- |
| [Clone](../../aspose.words.vba/vbaproject/clone/)() | Выполняет копирование`VbaProject` . |

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
