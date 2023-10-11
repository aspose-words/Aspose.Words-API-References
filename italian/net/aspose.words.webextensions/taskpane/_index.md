---
title: Class TaskPane
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.WebExtensions.TaskPane classe. Rappresenta un oggetto del riquadro attività del componente aggiuntivo.
type: docs
weight: 6710
url: /it/net/aspose.words.webextensions/taskpane/
---
## TaskPane class

Rappresenta un oggetto del riquadro attività del componente aggiuntivo.

Per saperne di più, visita il[Lavora con i componenti aggiuntivi di Office](https://docs.aspose.com/words/net/work-with-office-add-ins/) articolo di documentazione.

```csharp
public class TaskPane
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [TaskPane](taskpane/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DockState](../../aspose.words.webextensions/taskpane/dockstate/) { get; set; } | Specifica l'ultima posizione ancorata di questo oggetto del riquadro attività. |
| [IsLocked](../../aspose.words.webextensions/taskpane/islocked/) { get; set; } | Specifica se il riquadro attività è bloccato sul documento nell'interfaccia utente e non può essere chiuso dall'utente. |
| [IsVisible](../../aspose.words.webextensions/taskpane/isvisible/) { get; set; } | Specifica se il riquadro attività viene visualizzato come visibile per impostazione predefinita all'apertura del documento. |
| [Row](../../aspose.words.webextensions/taskpane/row/) { get; set; } | Specifica l'indice, enumerato dall'esterno verso l'interno, di questo riquadro attività tra gli altri riquadri attività persistented ancorati nella stessa posizione predefinita. |
| [WebExtension](../../aspose.words.webextensions/taskpane/webextension/) { get; } | Rappresenta un oggetto estensione web. |
| [Width](../../aspose.words.webextensions/taskpane/width/) { get; set; } | Specifica il valore di larghezza predefinito per questa istanza del riquadro attività. |

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

* spazio dei nomi [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* assemblea [Aspose.Words](../../)


