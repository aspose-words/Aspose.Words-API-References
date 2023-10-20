---
title: WebExtensionStoreType Enum
linktitle: WebExtensionStoreType
articleTitle: WebExtensionStoreType
second_title: Aspose.Words для .NET
description: Aspose.Words.WebExtensions.WebExtensionStoreType перечисление. Перечисляет доступные типы магазина вебрасширений на С#.
type: docs
weight: 6820
url: /ru/net/aspose.words.webextensions/webextensionstoretype/
---
## WebExtensionStoreType enumeration

Перечисляет доступные типы магазина веб-расширений.

```csharp
public enum WebExtensionStoreType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| SPCatalog | `0` | Указывает, что типом хранилища является корпоративный каталог SharePoint. |
| OMEX | `1` | Указывает, что тип магазина — Office.com. . |
| SPApp | `2` | Указывает, что типом хранилища является веб-приложение SharePoint. |
| Exchange | `3` | Указывает, что типом хранилища является сервер Exchange. |
| FileSystem | `4` | Указывает, что тип хранилища является общим ресурсом файловой системы. |
| Registry | `5` | Указывает, что типом хранилища является системный реестр. |
| ExCatalog | `6` | Указывает, что тип хранилища — централизованное развертывание через Exchange. |
| Default | `0` | Значение по умолчанию. |

## Примеры

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
