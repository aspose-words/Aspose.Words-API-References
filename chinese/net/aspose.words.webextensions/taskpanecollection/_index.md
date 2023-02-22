---
title: Class TaskPaneCollection
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.WebExtensions.TaskPaneCollection 班级. 指定持久任务窗格对象的列表
type: docs
weight: 6410
url: /zh/net/aspose.words.webextensions/taskpanecollection/
---
## TaskPaneCollection class

指定持久任务窗格对象的列表。

```csharp
public class TaskPaneCollection : BaseWebExtensionCollection<TaskPane>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.webextensions/basewebextensioncollection-1/count/) { get; } |  |
| [Item](../../aspose.words.webextensions/basewebextensioncollection-1/item/) { get; set; } |  |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words.webextensions/basewebextensioncollection-1/add/)(TaskPane) |  |
| [Clear](../../aspose.words.webextensions/basewebextensioncollection-1/clear/)() |  |
| [GetEnumerator](../../aspose.words.webextensions/basewebextensioncollection-1/getenumerator/)() |  |
| [Remove](../../aspose.words.webextensions/basewebextensioncollection-1/remove/)(int) |  |

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

* class [BaseWebExtensionCollection&lt;T&gt;](../basewebextensioncollection-1/)
* class [TaskPane](../taskpane/)
* 命名空间 [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* 部件 [Aspose.Words](../../)


