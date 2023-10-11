---
title: Class WebExtensionBindingCollection
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.WebExtensions.WebExtensionBindingCollection sınıf. Web uzantısı bağlamalarının listesini belirtir.
type: docs
weight: 6760
url: /tr/net/aspose.words.webextensions/webextensionbindingcollection/
---
## WebExtensionBindingCollection class

Web uzantısı bağlamalarının listesini belirtir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Office Eklentileriyle Çalışma](https://docs.aspose.com/words/net/work-with-office-add-ins/) dokümantasyon makalesi.

```csharp
public class WebExtensionBindingCollection : BaseWebExtensionCollection<WebExtensionBinding>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.webextensions/basewebextensioncollection-1/count/) { get; } |  |
| [Item](../../aspose.words.webextensions/basewebextensioncollection-1/item/) { get; set; } |  |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.webextensions/basewebextensioncollection-1/add/)(WebExtensionBinding) |  |
| [Clear](../../aspose.words.webextensions/basewebextensioncollection-1/clear/)() |  |
| [GetEnumerator](../../aspose.words.webextensions/basewebextensioncollection-1/getenumerator/)() |  |
| [Remove](../../aspose.words.webextensions/basewebextensioncollection-1/remove/)(int) |  |

### Örnekler

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

* class [BaseWebExtensionCollection&lt;T&gt;](../basewebextensioncollection-1/)
* class [WebExtensionBinding](../webextensionbinding/)
* ad alanı [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* toplantı [Aspose.Words](../../)


