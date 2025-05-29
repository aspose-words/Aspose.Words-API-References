---
title: WebExtensionBinding
linktitle: WebExtensionBinding
articleTitle: WebExtensionBinding
second_title: Aspose.Words for .NET
description: 使用 WebExtensionBinding 构造函数轻松创建强大的 Web 扩展绑定。自定义参数以实现无缝集成和增强功能。
type: docs
weight: 10
url: /zh/net/aspose.words.webextensions/webextensionbinding/webextensionbinding/
---
## WebExtensionBinding constructor

使用指定参数创建 Web 扩展绑定。

```csharp
public WebExtensionBinding(string id, WebExtensionBindingType bindingType, string appRef)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| id | String | 绑定标识符。 |
| bindingType | WebExtensionBindingType | 绑定类型。 |
| appRef | String | 绑定键用于将此列表中的绑定条目与文档中的绑定数据进行映射。 |

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

* enum [WebExtensionBindingType](../../webextensionbindingtype/)
* class [WebExtensionBinding](../)
* 命名空间 [Aspose.Words.WebExtensions](../../../aspose.words.webextensions/)
* 部件 [Aspose.Words](../../../)
