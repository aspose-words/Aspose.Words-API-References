---
title: WebExtensionReference Class
linktitle: WebExtensionReference
articleTitle: WebExtensionReference
second_title: .NET için Aspose.Words
description: Web uzantılarını kolaylıkla yönetmenin anahtarı olan Aspose.Words.WebExtensionReference sınıfını keşfedin. Sağlayıcıları ve sürümleri zahmetsizce belirleyin!
type: docs
weight: 7650
url: /tr/net/aspose.words.webextensions/webextensionreference/
---
## WebExtensionReference class

Bir web uzantısına referansı temsil eder. Referans, uzantısının sağlayıcı konumunu ve sürümünü tanımlamak için kullanılır.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Office Eklentileriyle Çalışın](https://docs.aspose.com/words/net/work-with-office-add-ins/) belgeleme makalesi.

```csharp
public class WebExtensionReference
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [WebExtensionReference](webextensionreference/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Id](../../aspose.words.webextensions/webextensionreference/id/) { get; set; } | Bir katalog sağlayıcısı içindeki web uzantısıyla ilişkili tanımlayıcı. |
| [Store](../../aspose.words.webextensions/webextensionreference/store/) { get; set; } | Web uzantısının depolandığı pazaryerinin örneğini belirtir. |
| [StoreType](../../aspose.words.webextensions/webextensionreference/storetype/) { get; set; } | Pazar yerinin türünü belirtir. |
| [Version](../../aspose.words.webextensions/webextensionreference/version/) { get; set; } | Web uzantısının sürümünü belirtir. |

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
