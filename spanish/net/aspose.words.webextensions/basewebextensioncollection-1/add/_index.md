---
title: BaseWebExtensionCollection1.Add
second_title: Referencia de API de Aspose.Words para .NET
description: BaseWebExtensionCollection método. Agrega el elemento especificado a la colección.
type: docs
weight: 30
url: /es/net/aspose.words.webextensions/basewebextensioncollection-1/add/
---
## BaseWebExtensionCollection&lt;T&gt;.Add method

Agrega el elemento especificado a la colección.

```csharp
public void Add(T item)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| item | T | Elemento para agregar. |

### Ejemplos

Muestra cómo agregar una extensión web a un documento.

```csharp
Document doc = new Document();

// Crear un panel de tareas con el complemento "MyScript", que será utilizado por el documento,
// luego establezca su ubicación predeterminada.
TaskPane myScriptTaskPane = new TaskPane();
doc.WebExtensionTaskPanes.Add(myScriptTaskPane);
myScriptTaskPane.DockState = TaskPaneDockState.Right;
myScriptTaskPane.IsVisible = true;
myScriptTaskPane.Width = 300;
myScriptTaskPane.IsLocked = true;

// Si hay varios paneles de tareas en la misma ubicación de acoplamiento, podemos establecer este índice para organizarlos.
myScriptTaskPane.Row = 1;

// Cree un complemento llamado "MyScript Math Sample", dentro del cual se mostrará el panel de tareas.
WebExtension webExtension = myScriptTaskPane.WebExtension;

// Establecer parámetros de referencia del almacén de aplicaciones para nuestro complemento, como el ID.
webExtension.Reference.Id = "WA104380646";
webExtension.Reference.Version = "1.0.0.0";
webExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
webExtension.Reference.Store = CultureInfo.CurrentCulture.Name;
webExtension.Properties.Add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
webExtension.Bindings.Add(new WebExtensionBinding("MyScript", WebExtensionBindingType.Text, "104380646"));

// Permitir que el usuario interactúe con el complemento.
webExtension.IsFrozen = false;

// Podemos acceder a la extensión web en Microsoft Word a través de Desarrollador -> Complementos.
doc.Save(ArtifactsDir + "Document.WebExtension.docx");

// Eliminar todos los paneles de tareas de la extensión web a la vez de esta manera.
doc.WebExtensionTaskPanes.Clear();

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Ver también

* class [BaseWebExtensionCollection&lt;T&gt;](../)
* espacio de nombres [Aspose.Words.WebExtensions](../../basewebextensioncollection-1/)
* asamblea [Aspose.Words](../../../)


