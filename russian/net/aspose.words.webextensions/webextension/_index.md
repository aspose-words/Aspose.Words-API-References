---
title: Class WebExtension
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.WebExtensions.WebExtension сорт. Представляет объект вебрасширения.
type: docs
weight: 6740
url: /ru/net/aspose.words.webextensions/webextension/
---
## WebExtension class

Представляет объект веб-расширения.

Чтобы узнать больше, посетите[Работа с надстройками Office](https://docs.aspose.com/words/net/work-with-office-add-ins/) статья документации.

```csharp
public class WebExtension
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [AlternateReferences](../../aspose.words.webextensions/webextension/alternatereferences/) { get; } | Указывает альтернативные ссылки на веб-расширение. |
| [Bindings](../../aspose.words.webextensions/webextension/bindings/) { get; } | Указывает список привязок веб-расширений. |
| [Id](../../aspose.words.webextensions/webextension/id/) { get; set; } | Уникально идентифицирует экземпляр веб-расширения в текущем документе. |
| [IsFrozen](../../aspose.words.webextensions/webextension/isfrozen/) { get; set; } | Указывает, может ли пользователь взаимодействовать с веб-расширением или нет. |
| [Properties](../../aspose.words.webextensions/webextension/properties/) { get; } | Представляет набор пользовательских свойств веб-расширения. |
| [Reference](../../aspose.words.webextensions/webextension/reference/) { get; } | Указывает основную ссылку на веб-расширение. |

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


