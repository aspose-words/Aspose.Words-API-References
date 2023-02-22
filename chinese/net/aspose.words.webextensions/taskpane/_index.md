---
title: Class TaskPane
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.WebExtensions.TaskPane 班级. 表示加载项任务窗格对象
type: docs
weight: 6400
url: /zh/net/aspose.words.webextensions/taskpane/
---
## TaskPane class

表示加载项任务窗格对象。

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
| [IsLocked](../../aspose.words.webextensions/taskpane/islocked/) { get; set; } | 指定任务窗格是否锁定到 UI 中的文档，并且用户不能关闭。 |
| [IsVisible](../../aspose.words.webextensions/taskpane/isvisible/) { get; set; } | 指定文档打开时任务窗格是否默认显示为可见。 |
| [Row](../../aspose.words.webextensions/taskpane/row/) { get; set; } | 指定此任务窗格的索引，从外到内枚举，以及停靠在同一默认位置的其他persisted 任务窗格。 |
| [WebExtension](../../aspose.words.webextensions/taskpane/webextension/) { get; } | 表示一个 Web 扩展对象。 |
| [Width](../../aspose.words.webextensions/taskpane/width/) { get; set; } | 指定此任务窗格实例的默认宽度值。 |

### 例子

展示如何向文档添加 Web 扩展。

```csharp
Document doc = new Document();

// 使用“MyScript”插件创建任务窗格，文档将使用该插件，
// 然后设置它的默认位置。
TaskPane myScriptTaskPane = new TaskPane();
doc.WebExtensionTaskPanes.Add(myScriptTaskPane);
myScriptTaskPane.DockState = TaskPaneDockState.Right;
myScriptTaskPane.IsVisible = true;
myScriptTaskPane.Width = 300;
myScriptTaskPane.IsLocked = true;

// 如果同一个停靠位置有多个任务窗格，我们可以设置这个索引来排列它们。
myScriptTaskPane.Row = 1;

// 创建一个名为“MyScript Math Sample”的加载项，任务窗格将在其中显示。
WebExtension webExtension = myScriptTaskPane.WebExtension;

// 为我们的加载项设置应用商店引用参数，例如 ID。
webExtension.Reference.Id = "WA104380646";
webExtension.Reference.Version = "1.0.0.0";
webExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
webExtension.Reference.Store = CultureInfo.CurrentCulture.Name;
webExtension.Properties.Add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
webExtension.Bindings.Add(new WebExtensionBinding("MyScript", WebExtensionBindingType.Text, "104380646"));

// 允许用户与加载项交互。
webExtension.IsFrozen = false;

// 我们可以通过 Developer 访问 Microsoft Word 中的 Web 扩展 ->加载项。
doc.Save(ArtifactsDir + "Document.WebExtension.docx");

// 像这样一次删除所有 Web 扩展任务窗格。
doc.WebExtensionTaskPanes.Clear();

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### 也可以看看

* 命名空间 [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* 部件 [Aspose.Words](../../)


