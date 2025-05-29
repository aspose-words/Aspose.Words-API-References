---
title: TaskPane Class
linktitle: TaskPane
articleTitle: TaskPane
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.WebExtensions.TaskPane 类，这是创建强大的插件任务窗格以增强文档编辑和提高工作效率的关键。
type: docs
weight: 7560
url: /zh/net/aspose.words.webextensions/taskpane/
---
## TaskPane class

表示加载项任务窗格对象。

要了解更多信息，请访问[使用 Office 加载项](https://docs.aspose.com/words/net/work-with-office-add-ins/)文档文章。

```csharp
public class TaskPane
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [TaskPane](taskpane/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DockState](../../aspose.words.webextensions/taskpane/dockstate/) { get; set; } | 指定此任务窗格对象的最后停靠位置。 |
| [IsLocked](../../aspose.words.webextensions/taskpane/islocked/) { get; set; } | 指定任务窗格是否锁定到 UI 中的文档并且用户无法关闭。 |
| [IsVisible](../../aspose.words.webextensions/taskpane/isvisible/) { get; set; } | 指定文档打开时任务窗格是否默认显示为可见。 |
| [Row](../../aspose.words.webextensions/taskpane/row/) { get; set; } | 指定此任务窗格与其他停靠在同一默认位置的任务窗格之间的索引（从外到内枚举）。 |
| [WebExtension](../../aspose.words.webextensions/taskpane/webextension/) { get; } | 表示 Web 扩展对象。 |
| [Width](../../aspose.words.webextensions/taskpane/width/) { get; set; } | 指定此任务窗格实例的默认宽度值。 |

## 例子

展示如何向文档添加 Web 扩展。

```csharp
Document doc = new Document();

// 使用“MyScript”插件创建任务窗格，该插件将由文档使用，
// 然后设置其默认位置。
TaskPane myScriptTaskPane = new TaskPane();
doc.WebExtensionTaskPanes.Add(myScriptTaskPane);
myScriptTaskPane.DockState = TaskPaneDockState.Right;
myScriptTaskPane.IsVisible = true;
myScriptTaskPane.Width = 300;
myScriptTaskPane.IsLocked = true;

// 如果在同一个停靠位置有多个任务窗格，我们可以设置这个索引来排列它们。
myScriptTaskPane.Row = 1;

// 创建一个名为“MyScript Math Sample”的插件，任务窗格将显示在其中。
WebExtension webExtension = myScriptTaskPane.WebExtension;

// 为我们的插件设置应用商店参考参数，例如 ID。
webExtension.Reference.Id = "WA104380646";
webExtension.Reference.Version = "1.0.0.0";
webExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
webExtension.Reference.Store = CultureInfo.CurrentCulture.Name;
webExtension.Properties.Add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
webExtension.Bindings.Add(new WebExtensionBinding("MyScript", WebExtensionBindingType.Text, "104380646"));

// 允许用户与插件进行交互。
webExtension.IsFrozen = false;

// 我们可以通过开发人员 -> 插件访问 Microsoft Word 中的 Web 扩展。
doc.Save(ArtifactsDir + "Document.WebExtension.docx");

// 像这样一次性删除所有 Web 扩展任务窗格。
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

### 也可以看看

* 命名空间 [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* 部件 [Aspose.Words](../../)
