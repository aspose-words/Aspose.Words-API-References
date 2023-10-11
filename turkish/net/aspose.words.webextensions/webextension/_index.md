---
title: Class WebExtension
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.WebExtensions.WebExtension sınıf. Bir web uzantısı nesnesini temsil eder.
type: docs
weight: 6740
url: /tr/net/aspose.words.webextensions/webextension/
---
## WebExtension class

Bir web uzantısı nesnesini temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Office Eklentileriyle Çalışma](https://docs.aspose.com/words/net/work-with-office-add-ins/) dokümantasyon makalesi.

```csharp
public class WebExtension
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AlternateReferences](../../aspose.words.webextensions/webextension/alternatereferences/) { get; } | Bir web uzantısına alternatif referansları belirtir. |
| [Bindings](../../aspose.words.webextensions/webextension/bindings/) { get; } | Web uzantısı bağlamalarının listesini belirtir. |
| [Id](../../aspose.words.webextensions/webextension/id/) { get; set; } | Geçerli belgedeki web uzantısı örneğini benzersiz şekilde tanımlar. |
| [IsFrozen](../../aspose.words.webextensions/webextension/isfrozen/) { get; set; } | Kullanıcının web uzantısıyla etkileşimde bulunup bulunamayacağını belirtir. |
| [Properties](../../aspose.words.webextensions/webextension/properties/) { get; } | Bir dizi web uzantısı özel özelliğini temsil eder. |
| [Reference](../../aspose.words.webextensions/webextension/reference/) { get; } | Bir web uzantısına yönelik birincil referansı belirtir. |

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

* ad alanı [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* toplantı [Aspose.Words](../../)


