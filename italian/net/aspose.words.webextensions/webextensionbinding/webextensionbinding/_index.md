---
title: WebExtensionBinding.WebExtensionBinding
second_title: Aspose.Words per .NET API Reference
description: WebExtensionBinding costruttore. Crea lassociazione dellestensione web con i parametri specificati.
type: docs
weight: 10
url: /it/net/aspose.words.webextensions/webextensionbinding/webextensionbinding/
---
## WebExtensionBinding constructor

Crea l'associazione dell'estensione web con i parametri specificati.

```csharp
public WebExtensionBinding(string id, WebExtensionBindingType bindingType, string appRef)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| id | String | Identificatore vincolante. |
| bindingType | WebExtensionBindingType | Tipo di rilegatura. |
| appRef | String | Chiave di associazione utilizzata per associare la voce di associazione in questo elenco con i dati associati nel documento. |

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

* enum [WebExtensionBindingType](../../webextensionbindingtype/)
* class [WebExtensionBinding](../)
* spazio dei nomi [Aspose.Words.WebExtensions](../../webextensionbinding/)
* assemblea [Aspose.Words](../../../)


