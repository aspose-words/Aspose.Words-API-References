---
title: Enum WebExtensionStoreType
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.WebExtensions.WebExtensionStoreType enum. Enumera i tipi disponibili di un archivio di estensioni web.
type: docs
weight: 6820
url: /it/net/aspose.words.webextensions/webextensionstoretype/
---
## WebExtensionStoreType enumeration

Enumera i tipi disponibili di un archivio di estensioni web.

```csharp
public enum WebExtensionStoreType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| SPCatalog | `0` | Specifica che il tipo di negozio è il catalogo aziendale di SharePoint. |
| OMEX | `1` | Specifica che il tipo di negozio è Office.com. |
| SPApp | `2` | Specifica che il tipo di archivio è un'applicazione Web di SharePoint. |
| Exchange | `3` | Specifica che il tipo di archivio è un server Exchange. |
| FileSystem | `4` | Specifica che il tipo di archivio è una condivisione del file system. |
| Registry | `5` | Specifica che il tipo di archivio è il registro di sistema. |
| ExCatalog | `6` | Specifica che il tipo di archivio è Distribuzione centralizzata tramite Exchange. |
| Default | `0` | Valore predefinito. |

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


