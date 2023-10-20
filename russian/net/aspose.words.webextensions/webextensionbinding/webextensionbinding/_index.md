---
title: WebExtensionBinding
linktitle: WebExtensionBinding
articleTitle: WebExtensionBinding
second_title: Aspose.Words для .NET
description: WebExtensionBinding строитель. Создает привязку вебрасширения с указанными параметрами на С#.
type: docs
weight: 10
url: /ru/net/aspose.words.webextensions/webextensionbinding/webextensionbinding/
---
## WebExtensionBinding constructor

Создает привязку веб-расширения с указанными параметрами.

```csharp
public WebExtensionBinding(string id, WebExtensionBindingType bindingType, string appRef)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| id | String | Идентификатор привязки. |
| bindingType | WebExtensionBindingType | Тип привязки. |
| appRef | String | Ключ привязки, используемый для сопоставления записи привязки в этом списке с привязанными данными в документе. |

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

* enum [WebExtensionBindingType](../../webextensionbindingtype/)
* class [WebExtensionBinding](../)
* пространство имен [Aspose.Words.WebExtensions](../../../aspose.words.webextensions/)
* сборка [Aspose.Words](../../../)
