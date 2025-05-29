---
title: TaskPane Class
linktitle: TaskPane
articleTitle: TaskPane
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.WebExtensions.TaskPane — ваш ключ к созданию мощных надстроек панелей задач для расширенного редактирования документов и повышения производительности.
type: docs
weight: 7560
url: /ru/net/aspose.words.webextensions/taskpane/
---
## TaskPane class

Представляет объект области задач надстройки.

Чтобы узнать больше, посетите[Работа с надстройками Office](https://docs.aspose.com/words/net/work-with-office-add-ins/) документальная статья.

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
| [IsLocked](../../aspose.words.webextensions/taskpane/islocked/) { get; set; } | Указывает, заблокирована ли область задач для документа в пользовательском интерфейсе и не может ли пользователь закрыть ее. |
| [IsVisible](../../aspose.words.webextensions/taskpane/isvisible/) { get; set; } | Указывает, отображается ли панель задач по умолчанию при открытии документа. |
| [Row](../../aspose.words.webextensions/taskpane/row/) { get; set; } | Указывает индекс, перечисляя снаружи внутрь, этой области задач среди других сохраняемых областей задач, закрепленных в том же месте по умолчанию. |
| [WebExtension](../../aspose.words.webextensions/taskpane/webextension/) { get; } | Представляет объект веб-расширения. |
| [Width](../../aspose.words.webextensions/taskpane/width/) { get; set; } | Указывает значение ширины по умолчанию для этого экземпляра области задач. |

## Примеры

Показывает, как добавить веб-расширение к документу.

```csharp
Document doc = new Document();

// Создаем область задач с надстройкой "MyScript", которая будет использоваться документом,
// затем установите его местоположение по умолчанию.
TaskPane myScriptTaskPane = new TaskPane();
doc.WebExtensionTaskPanes.Add(myScriptTaskPane);
myScriptTaskPane.DockState = TaskPaneDockState.Right;
myScriptTaskPane.IsVisible = true;
myScriptTaskPane.Width = 300;
myScriptTaskPane.IsLocked = true;

// Если в одном месте закрепления находится несколько панелей задач, мы можем задать этот индекс для их упорядочивания.
myScriptTaskPane.Row = 1;

// Создайте надстройку с названием «MyScript Math Sample», которая будет отображаться на панели задач.
WebExtension webExtension = myScriptTaskPane.WebExtension;

// Задаем параметры ссылки на магазин приложений для нашей надстройки, такие как идентификатор.
webExtension.Reference.Id = "WA104380646";
webExtension.Reference.Version = "1.0.0.0";
webExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
webExtension.Reference.Store = CultureInfo.CurrentCulture.Name;
webExtension.Properties.Add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
webExtension.Bindings.Add(new WebExtensionBinding("MyScript", WebExtensionBindingType.Text, "104380646"));

// Разрешить пользователю взаимодействовать с надстройкой.
webExtension.IsFrozen = false;

// Мы можем получить доступ к веб-расширению в Microsoft Word через Developer -> Add-ins.
doc.Save(ArtifactsDir + "Document.WebExtension.docx");

// Удалить все панели задач веб-расширения сразу, как показано ниже.
doc.WebExtensionTaskPanes.Clear();

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);

doc = new Document(ArtifactsDir + "Document.WebExtension.docx");

myScriptTaskPane = doc.WebExtensionTaskPanes[0];
Assert.AreEqual(TaskPaneDockState.Right, myScriptTaskPane.DockState);
Assert.True(myScriptTaskPane.IsVisible);
Assert.AreEqual(300.0d, myScriptTaskPane.Width);
Assert.True(myScriptTaskPane.IsLocked);
Assert.AreEqual(1, myScriptTaskPane.Row);

webExtension = myScriptTaskPane.WebExtension;
Assert.AreEqual(string.Empty, webExtension.Id);

Assert.AreEqual("WA104380646", webExtension.Reference.Id);
Assert.AreEqual("1.0.0.0", webExtension.Reference.Version);
Assert.AreEqual(WebExtensionStoreType.OMEX, webExtension.Reference.StoreType);
Assert.AreEqual(CultureInfo.CurrentCulture.Name, webExtension.Reference.Store);
Assert.AreEqual(0, webExtension.AlternateReferences.Count);

Assert.AreEqual("MyScript", webExtension.Properties[0].Name);
Assert.AreEqual("MyScript Math Sample", webExtension.Properties[0].Value);

Assert.AreEqual("MyScript", webExtension.Bindings[0].Id);
Assert.AreEqual(WebExtensionBindingType.Text, webExtension.Bindings[0].BindingType);
Assert.AreEqual("104380646", webExtension.Bindings[0].AppRef);

Assert.False(webExtension.IsFrozen);
```

### Смотрите также

* пространство имен [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* сборка [Aspose.Words](../../)
