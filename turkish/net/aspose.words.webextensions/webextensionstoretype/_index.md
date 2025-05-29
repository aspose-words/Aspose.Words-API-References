---
title: WebExtensionStoreType Enum
linktitle: WebExtensionStoreType
articleTitle: WebExtensionStoreType
second_title: .NET için Aspose.Words
description: Kusursuz entegrasyon ve gelişmiş işlevsellik için çeşitli web uzantısı depolama türlerini içeren Aspose.Words.WebExtensionStoreType enum'unu keşfedin.
type: docs
weight: 7670
url: /tr/net/aspose.words.webextensions/webextensionstoretype/
---
## WebExtensionStoreType enumeration

Bir web uzantısı deposunun kullanılabilir türlerini sıralar.

```csharp
public enum WebExtensionStoreType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| SPCatalog | `0` | Mağaza türünün SharePoint kurumsal kataloğu olduğunu belirtir. |
| OMEX | `1` | Mağaza türünün Office.com olduğunu belirtir. |
| SPApp | `2` | Mağaza türünün bir SharePoint web uygulaması olduğunu belirtir. |
| Exchange | `3` | Mağaza türünün bir Exchange sunucusu olduğunu belirtir. |
| FileSystem | `4` | Depolama türünün bir dosya sistemi paylaşımı olduğunu belirtir. |
| Registry | `5` | Depolama türünün sistem kayıt defteri olduğunu belirtir. |
| ExCatalog | `6` | Mağaza türünün Exchange aracılığıyla Merkezi Dağıtım olduğunu belirtir. |
| Default | `0` | Varsayılan değer. |

## Örnekler

Bir belgeye web uzantısının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();

// Belge tarafından kullanılacak "MyScript" eklentisi ile görev bölmesini oluşturun,
// daha sonra varsayılan konumunu ayarlayın.
TaskPane myScriptTaskPane = new TaskPane();
doc.WebExtensionTaskPanes.Add(myScriptTaskPane);
myScriptTaskPane.DockState = TaskPaneDockState.Right;
myScriptTaskPane.IsVisible = true;
myScriptTaskPane.Width = 300;
myScriptTaskPane.IsLocked = true;

// Aynı yerleştirme konumunda birden fazla görev bölmesi varsa, bunları düzenlemek için bu dizini ayarlayabiliriz.
myScriptTaskPane.Row = 1;

// Görev bölmesinin içinde görüntülenecek "MyScript Math Sample" adında bir eklenti oluşturun.
WebExtension webExtension = myScriptTaskPane.WebExtension;

// Eklentimiz için ID gibi uygulama deposu referans parametrelerini ayarlayın.
webExtension.Reference.Id = "WA104380646";
webExtension.Reference.Version = "1.0.0.0";
webExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
webExtension.Reference.Store = CultureInfo.CurrentCulture.Name;
webExtension.Properties.Add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
webExtension.Bindings.Add(new WebExtensionBinding("MyScript", WebExtensionBindingType.Text, "104380646"));

// Kullanıcının eklentiyle etkileşime girmesine izin ver.
webExtension.IsFrozen = false;

// Microsoft Word'deki web uzantısına Geliştirici -> Eklentiler yoluyla erişebiliriz.
doc.Save(ArtifactsDir + "Document.WebExtension.docx");

// Tüm web uzantısı görev bölmelerini aynı anda bu şekilde kaldırın.
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

### Ayrıca bakınız

* ad alanı [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* toplantı [Aspose.Words](../../)
