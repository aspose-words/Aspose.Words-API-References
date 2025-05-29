---
title: WebExtensionReference Class
linktitle: WebExtensionReference
articleTitle: WebExtensionReference
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.WebExtensionReference, la chiave per gestire le estensioni web con facilità. Identifica provider e versioni senza sforzo!
type: docs
weight: 7650
url: /it/net/aspose.words.webextensions/webextensionreference/
---
## WebExtensionReference class

Rappresenta il riferimento a un'estensione web. Il riferimento viene utilizzato per identificare la posizione del provider e la versione dell'estensione .

Per saperne di più, visita il[Lavorare con i componenti aggiuntivi di Office](https://docs.aspose.com/words/net/work-with-office-add-ins/) articolo di documentazione.

```csharp
public class WebExtensionReference
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [WebExtensionReference](webextensionreference/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Id](../../aspose.words.webextensions/webextensionreference/id/) { get; set; } | Identificatore associato all'estensione web all'interno di un fornitore di cataloghi. |
| [Store](../../aspose.words.webextensions/webextensionreference/store/) { get; set; } | Specifica l'istanza del marketplace in cui è archiviata l'estensione web. |
| [StoreType](../../aspose.words.webextensions/webextensionreference/storetype/) { get; set; } | Specifica il tipo di mercato. |
| [Version](../../aspose.words.webextensions/webextensionreference/version/) { get; set; } | Specifica la versione dell'estensione web. |

## Esempi

Mostra come aggiungere un'estensione web a un documento.

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

// Se ci sono più riquadri attività nella stessa posizione di ancoraggio, possiamo impostare questo indice per disporli.
myScriptTaskPane.Row = 1;

// Crea un componente aggiuntivo denominato "MyScript Math Sample", che verrà visualizzato nel riquadro delle attività.
WebExtension webExtension = myScriptTaskPane.WebExtension;

// Imposta i parametri di riferimento dell'app store per il nostro componente aggiuntivo, come l'ID.
webExtension.Reference.Id = "WA104380646";
webExtension.Reference.Version = "1.0.0.0";
webExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
webExtension.Reference.Store = CultureInfo.CurrentCulture.Name;
webExtension.Properties.Add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
webExtension.Bindings.Add(new WebExtensionBinding("MyScript", WebExtensionBindingType.Text, "104380646"));

// Consenti all'utente di interagire con il componente aggiuntivo.
webExtension.IsFrozen = false;

// Possiamo accedere all'estensione web in Microsoft Word tramite Sviluppatore -> Componenti aggiuntivi.
doc.Save(ArtifactsDir + "Document.WebExtension.docx");

// Rimuovi tutti i riquadri attività dell'estensione web in una volta sola, in questo modo.
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

### Guarda anche

* spazio dei nomi [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* assemblea [Aspose.Words](../../)
