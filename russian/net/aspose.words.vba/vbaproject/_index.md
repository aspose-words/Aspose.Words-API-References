---
title: VbaProject Class
linktitle: VbaProject
articleTitle: VbaProject
second_title: Aspose.Words для .NET
description: Aspose.Words.Vba.VbaProject сорт. Обеспечивает доступ к информации о проекте VBA. Проект VBA внутри документа определяется как набор модулей VBA на С#.
type: docs
weight: 6580
url: /ru/net/aspose.words.vba/vbaproject/
---
## VbaProject class

Обеспечивает доступ к информации о проекте VBA. Проект VBA внутри документа определяется как набор модулей VBA.

Чтобы узнать больше, посетите[Работа с макросами VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) статья документации.

```csharp
public class VbaProject
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [VbaProject](vbaproject/)() | Создает пробел`VbaProject` . |

## Характеристики

| Имя | Описание |
| --- | --- |
| [CodePage](../../aspose.words.vba/vbaproject/codepage/) { get; set; } | Получает или задает кодовую страницу проекта VBA. |
| [IsSigned](../../aspose.words.vba/vbaproject/issigned/) { get; } | Показывает,`VbaProject` подписан или нет. |
| [Modules](../../aspose.words.vba/vbaproject/modules/) { get; } | Возвращает коллекцию модулей проекта VBA. |
| [Name](../../aspose.words.vba/vbaproject/name/) { get; set; } | Получает или задает имя проекта VBA. |
| [References](../../aspose.words.vba/vbaproject/references/) { get; } | Получает коллекцию ссылок на проекты VBA. |

## Методы

| Имя | Описание |
| --- | --- |
| [Clone](../../aspose.words.vba/vbaproject/clone/)() | Выполняет копию`VbaProject` . |

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

* пространство имен [Aspose.Words.Vba](../../aspose.words.vba/)
* сборка [Aspose.Words](../../)
