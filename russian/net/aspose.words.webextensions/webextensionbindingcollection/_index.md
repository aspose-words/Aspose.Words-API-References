---
title: WebExtensionBindingCollection Class
linktitle: WebExtensionBindingCollection
articleTitle: WebExtensionBindingCollection
second_title: Aspose.Words для .NET
description: Aspose.Words.WebExtensions.WebExtensionBindingCollection сорт. Указывает список привязок вебрасширений на С#.
type: docs
weight: 6760
url: /ru/net/aspose.words.webextensions/webextensionbindingcollection/
---
## WebExtensionBindingCollection class

Указывает список привязок веб-расширений.

Чтобы узнать больше, посетите[Работа с надстройками Office](https://docs.aspose.com/words/net/work-with-office-add-ins/) статья документации.

```csharp
public class WebExtensionBindingCollection : BaseWebExtensionCollection<WebExtensionBinding>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.webextensions/basewebextensioncollection-1/count/) { get; } |  |
| [Item](../../aspose.words.webextensions/basewebextensioncollection-1/item/) { get; set; } |  |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words.webextensions/basewebextensioncollection-1/add/)(*[WebExtensionBinding](../webextensionbinding/)*) |  |
| [Clear](../../aspose.words.webextensions/basewebextensioncollection-1/clear/)() |  |
| [GetEnumerator](../../aspose.words.webextensions/basewebextensioncollection-1/getenumerator/)() |  |
| [Remove](../../aspose.words.webextensions/basewebextensioncollection-1/remove/)(*int*) |  |

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

* class [BaseWebExtensionCollection&lt;T&gt;](../basewebextensioncollection-1/)
* class [WebExtensionBinding](../webextensionbinding/)
* пространство имен [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* сборка [Aspose.Words](../../)
