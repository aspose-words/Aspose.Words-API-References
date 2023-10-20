---
title: WebExtensionStoreType Enum
linktitle: WebExtensionStoreType
articleTitle: WebExtensionStoreType
second_title: Aspose.Words for .NET
description: Aspose.Words.WebExtensions.WebExtensionStoreType Sıralama. Web uzantısı deposunun kullanılabilir türlerini numaralandırır C#'da.
type: docs
weight: 6820
url: /tr/net/aspose.words.webextensions/webextensionstoretype/
---
## WebExtensionStoreType enumeration

Web uzantısı deposunun kullanılabilir türlerini numaralandırır.

```csharp
public enum WebExtensionStoreType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| SPCatalog | `0` | Mağaza türünün SharePoint kurumsal kataloğu olduğunu belirtir. |
| OMEX | `1` | Mağaza türünün Office.com. olduğunu belirtir |
| SPApp | `2` | Mağaza türünün bir SharePoint web uygulaması olduğunu belirtir. |
| Exchange | `3` | Mağaza türünün bir Exchange sunucusu olduğunu belirtir. |
| FileSystem | `4` | Mağaza türünün bir dosya sistemi paylaşımı olduğunu belirtir. |
| Registry | `5` | Mağaza türünün sistem kayıt defteri olduğunu belirtir. |
| ExCatalog | `6` | Mağaza türünün Exchange Aracılığıyla Merkezi Dağıtım olduğunu belirtir. |
| Default | `0` | Varsayılan değer. |

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

* ad alanı [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* toplantı [Aspose.Words](../../)
