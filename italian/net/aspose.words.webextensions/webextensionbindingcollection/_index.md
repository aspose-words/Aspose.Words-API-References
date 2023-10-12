---
title: Class WebExtensionBindingCollection
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.WebExtensions.WebExtensionBindingCollection classe. Specifica un elenco di associazioni di estensioni web.
type: docs
weight: 6760
url: /it/net/aspose.words.webextensions/webextensionbindingcollection/
---
## WebExtensionBindingCollection class

Specifica un elenco di associazioni di estensioni web.

Per saperne di più, visita il[Lavora con i componenti aggiuntivi di Office](https://docs.aspose.com/words/net/work-with-office-add-ins/) articolo di documentazione.

```csharp
public class WebExtensionBindingCollection : BaseWebExtensionCollection<WebExtensionBinding>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.webextensions/basewebextensioncollection-1/count/) { get; } |  |
| [Item](../../aspose.words.webextensions/basewebextensioncollection-1/item/) { get; set; } |  |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words.webextensions/basewebextensioncollection-1/add/)(WebExtensionBinding) |  |
| [Clear](../../aspose.words.webextensions/basewebextensioncollection-1/clear/)() |  |
| [GetEnumerator](../../aspose.words.webextensions/basewebextensioncollection-1/getenumerator/)() |  |
| [Remove](../../aspose.words.webextensions/basewebextensioncollection-1/remove/)(int) |  |

### Esempi

Mostra come aggiungere un'estensione Web a un documento.

```csharp
Document doc = new Document();

// Crea il riquadro attività con il componente aggiuntivo "MyScript", che verrà utilizzato dal documento,
// quindi imposta la sua posizione predefinita.
TaskPane myScriptTaskPane = new TaskPane();
doc.WebExtensionTaskPanes.Add(myScriptTaskPane);
myScriptTaskPane.DockState = TaskPaneDockState.Right;
myScriptTaskPane.IsVisible = true;
myScriptTaskPane.Width = 300;
myScriptTaskPane.IsLocked = true;

// Se sono presenti più riquadri attività nella stessa posizione di ancoraggio, è possibile impostare questo indice per organizzarli.
myScriptTaskPane.Row = 1;

// Crea un componente aggiuntivo chiamato "MyScript Math Sample", all'interno del quale verrà visualizzato il riquadro attività.
WebExtension webExtension = myScriptTaskPane.WebExtension;

// Imposta i parametri di riferimento dell'archivio applicazioni per il nostro componente aggiuntivo, come l'ID.
webExtension.Reference.Id = "WA104380646";
webExtension.Reference.Version = "1.0.0.0";
webExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
webExtension.Reference.Store = CultureInfo.CurrentCulture.Name;
webExtension.Properties.Add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
webExtension.Bindings.Add(new WebExtensionBinding("MyScript", WebExtensionBindingType.Text, "104380646"));

// Consentire all'utente di interagire con il componente aggiuntivo.
webExtension.IsFrozen = false;

// Possiamo accedere all'estensione web in Microsoft Word tramite Developer -> Componenti aggiuntivi.
doc.Save(ArtifactsDir + "Document.WebExtension.docx");

// Rimuovi tutti i riquadri attività delle estensioni Web contemporaneamente in questo modo.
doc.WebExtensionTaskPanes.Clear();

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Guarda anche

* class [BaseWebExtensionCollection&lt;T&gt;](../basewebextensioncollection-1/)
* class [WebExtensionBinding](../webextensionbinding/)
* spazio dei nomi [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* assemblea [Aspose.Words](../../)


