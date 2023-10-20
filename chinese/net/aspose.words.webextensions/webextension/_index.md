---
title: WebExtension Class
linktitle: WebExtension
articleTitle: WebExtension
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.WebExtensions.WebExtension 班级. 表示一个 Web 扩展对象 在 C#.
type: docs
weight: 6740
url: /zh/net/aspose.words.webextensions/webextension/
---
## WebExtension class

表示一个 Web 扩展对象。

```csharp
public class WebExtension
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AlternateReferences](../../aspose.words.webextensions/webextension/alternatereferences/) { get; } | 指定对 Web 扩展的替代引用。 |
| [Bindings](../../aspose.words.webextensions/webextension/bindings/) { get; } | 指定 Web 扩展绑定列表。 |
| [Id](../../aspose.words.webextensions/webextension/id/) { get; set; } | 唯一标识当前文档中的 Web 扩展实例。 |
| [IsFrozen](../../aspose.words.webextensions/webextension/isfrozen/) { get; set; } | 指定用户是否可以与 Web 扩展交互。 |
| [Properties](../../aspose.words.webextensions/webextension/properties/) { get; } | 表示一组 Web 扩展自定义属性。 |
| [Reference](../../aspose.words.webextensions/webextension/reference/) { get; } | 指定对 Web 扩展的主要引用。 |

## 例子

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
