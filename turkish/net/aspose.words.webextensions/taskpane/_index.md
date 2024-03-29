---
title: TaskPane Class
linktitle: TaskPane
articleTitle: TaskPane
second_title: Aspose.Words for .NET
description: Aspose.Words.WebExtensions.TaskPane sınıf. Eklenti görev bölmesi nesnesini temsil eder C#'da.
type: docs
weight: 6710
url: /tr/net/aspose.words.webextensions/taskpane/
---
## TaskPane class

Eklenti görev bölmesi nesnesini temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Office Eklentileriyle Çalışma](https://docs.aspose.com/words/net/work-with-office-add-ins/) dokümantasyon makalesi.

```csharp
public class TaskPane
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [TaskPane](taskpane/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DockState](../../aspose.words.webextensions/taskpane/dockstate/) { get; set; } | Bu görev bölmesi nesnesinin en son yerleştirildiği konumu belirtir. |
| [IsLocked](../../aspose.words.webextensions/taskpane/islocked/) { get; set; } | Görev bölmesinin kullanıcı arayüzündeki belgeye kilitli olup olmadığını ve kullanıcı tarafından kapatılıp kapatılamayacağını belirtir. |
| [IsVisible](../../aspose.words.webextensions/taskpane/isvisible/) { get; set; } | Belge açıldığında görev bölmesinin varsayılan olarak görünür olarak görünüp görünmeyeceğini belirtir. |
| [Row](../../aspose.words.webextensions/taskpane/row/) { get; set; } | Aynı varsayılan konuma yerleştirilmiş diğer persisted görev bölmeleri arasında bu görev bölmesinin dışarıdan içeriye doğru numaralandırılan dizinini belirtir. |
| [WebExtension](../../aspose.words.webextensions/taskpane/webextension/) { get; } | Bir web uzantısı nesnesini temsil eder. |
| [Width](../../aspose.words.webextensions/taskpane/width/) { get; set; } | Bu görev bölmesi örneği için varsayılan genişlik değerini belirtir. |

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
