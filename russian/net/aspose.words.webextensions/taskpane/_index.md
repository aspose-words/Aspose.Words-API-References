---
title: Class TaskPane
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.WebExtensions.TaskPane сорт. Представляет объект области задач надстройки.
type: docs
weight: 6710
url: /ru/net/aspose.words.webextensions/taskpane/
---
## TaskPane class

Представляет объект области задач надстройки.

Чтобы узнать больше, посетите[Работа с надстройками Office](https://docs.aspose.com/words/net/work-with-office-add-ins/) статья документации.

```csharp
public class TaskPane
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [TaskPane](taskpane/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [DockState](../../aspose.words.webextensions/taskpane/dockstate/) { get; set; } | Указывает последнее закрепленное местоположение этого объекта области задач. |
| [IsLocked](../../aspose.words.webextensions/taskpane/islocked/) { get; set; } | Указывает, привязана ли панель задач к документу в пользовательском интерфейсе и не может быть закрыта пользователем. |
| [IsVisible](../../aspose.words.webextensions/taskpane/isvisible/) { get; set; } | Указывает, отображается ли панель задач видимой по умолчанию при открытии документа. |
| [Row](../../aspose.words.webextensions/taskpane/row/) { get; set; } | Указывает индекс этой панели задач, перечисляемый снаружи внутрь, среди других панелей задач persisted , закрепленных в том же месте по умолчанию. |
| [WebExtension](../../aspose.words.webextensions/taskpane/webextension/) { get; } | Представляет объект веб-расширения. |
| [Width](../../aspose.words.webextensions/taskpane/width/) { get; set; } | Указывает значение ширины по умолчанию для этого экземпляра области задач. |

### Примеры

Показывает, как добавить веб-расширение в документ.

```csharp
Document doc = new Document();

// Создаём панель задач с надстройкой MyScript, которая будет использоваться документом,
// затем устанавливаем местоположение по умолчанию.
TaskPane myScriptTaskPane = new TaskPane();
doc.WebExtensionTaskPanes.Add(myScriptTaskPane);
myScriptTaskPane.DockState = TaskPaneDockState.Right;
myScriptTaskPane.IsVisible = true;
myScriptTaskPane.Width = 300;
myScriptTaskPane.IsLocked = true;

// Если в одном месте закрепления находится несколько панелей задач, мы можем установить этот индекс, чтобы упорядочить их.
myScriptTaskPane.Row = 1;

// Создайте надстройку под названием «MyScript Math Sample», внутри которой будет отображаться панель задач.
WebExtension webExtension = myScriptTaskPane.WebExtension;

// Установите ссылочные параметры хранилища приложений для нашей надстройки, например идентификатор.
webExtension.Reference.Id = "WA104380646";
webExtension.Reference.Version = "1.0.0.0";
webExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
webExtension.Reference.Store = CultureInfo.CurrentCulture.Name;
webExtension.Properties.Add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
webExtension.Bindings.Add(new WebExtensionBinding("MyScript", WebExtensionBindingType.Text, "104380646"));

// Разрешить пользователю взаимодействовать с надстройкой.
webExtension.IsFrozen = false;

// Мы можем получить доступ к веб-расширению в Microsoft Word через Developer -> gt; Надстройки.
doc.Save(ArtifactsDir + "Document.WebExtension.docx");

// Удалить все панели задач веб-расширений одновременно, вот так.
doc.WebExtensionTaskPanes.Clear();

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Смотрите также

* пространство имен [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* сборка [Aspose.Words](../../)


