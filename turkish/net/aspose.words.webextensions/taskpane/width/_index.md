---
title: TaskPane.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words for .NET
description: TaskPane Width mülk. Bu görev bölmesi örneği için varsayılan genişlik değerini belirtir C#'da.
type: docs
weight: 70
url: /tr/net/aspose.words.webextensions/taskpane/width/
---
## TaskPane.Width property

Bu görev bölmesi örneği için varsayılan genişlik değerini belirtir.

```csharp
public double Width { get; set; }
```

## Örnekler

Bir belgeye nasıl web uzantısı ekleneceğini gösterir.

```csharp
Document doc = new Document();

// Dokümanın kullanacağı "MyScript" eklentisi ile görev bölmesi oluşturalım,
// daha sonra varsayılan konumunu ayarlayın.
TaskPane myScriptTaskPane = new TaskPane();
doc.WebExtensionTaskPanes.Add(myScriptTaskPane);
myScriptTaskPane.DockState = TaskPaneDockState.Right;
myScriptTaskPane.IsVisible = true;
myScriptTaskPane.Width = 300;
myScriptTaskPane.IsLocked = true;

// Aynı yerleştirme konumunda birden fazla görev bölmesi varsa, bunları düzenlemek için bu dizini ayarlayabiliriz.
myScriptTaskPane.Row = 1;

// Görev bölmesinin içinde görüntüleyeceği "MyScript Math Sample" adında bir eklenti oluşturun.
WebExtension webExtension = myScriptTaskPane.WebExtension;

// Eklentimiz için ID gibi uygulama mağazası referans parametrelerini ayarlayın.
webExtension.Reference.Id = "WA104380646";
webExtension.Reference.Version = "1.0.0.0";
webExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
webExtension.Reference.Store = CultureInfo.CurrentCulture.Name;
webExtension.Properties.Add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
webExtension.Bindings.Add(new WebExtensionBinding("MyScript", WebExtensionBindingType.Text, "104380646"));

// Kullanıcının eklentiyle etkileşime girmesine izin ver.
webExtension.IsFrozen = false;

// Microsoft Word'deki web uzantısına Developer --> aracılığıyla erişebiliriz. Eklentiler.
doc.Save(ArtifactsDir + "Document.WebExtension.docx");

// Tüm web uzantısı görev bölmelerini bu şekilde bir kerede kaldırın.
doc.WebExtensionTaskPanes.Clear();

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Ayrıca bakınız

* class [TaskPane](../)
* ad alanı [Aspose.Words.WebExtensions](../../../aspose.words.webextensions/)
* toplantı [Aspose.Words](../../../)
