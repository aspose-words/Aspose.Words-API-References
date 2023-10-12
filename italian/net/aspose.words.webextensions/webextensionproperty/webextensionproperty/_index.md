---
title: WebExtensionProperty.WebExtensionProperty
second_title: Aspose.Words per .NET API Reference
description: WebExtensionProperty costruttore. Crea la proprietà personalizzata dellestensione web con il nome e il valore specificati.
type: docs
weight: 10
url: /it/net/aspose.words.webextensions/webextensionproperty/webextensionproperty/
---
## WebExtensionProperty constructor

Crea la proprietà personalizzata dell'estensione web con il nome e il valore specificati.

```csharp
public WebExtensionProperty(string name, string value)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | String | Nome della proprietà. |
| value | String | Costo dell'immobile. |

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

* class [WebExtensionProperty](../)
* spazio dei nomi [Aspose.Words.WebExtensions](../../webextensionproperty/)
* assemblea [Aspose.Words](../../../)


