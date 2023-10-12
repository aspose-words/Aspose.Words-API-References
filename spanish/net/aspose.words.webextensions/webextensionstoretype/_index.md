---
title: Enum WebExtensionStoreType
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.WebExtensions.WebExtensionStoreType enumeración. Enumera los tipos disponibles de una tienda de extensiones web.
type: docs
weight: 6820
url: /es/net/aspose.words.webextensions/webextensionstoretype/
---
## WebExtensionStoreType enumeration

Enumera los tipos disponibles de una tienda de extensiones web.

```csharp
public enum WebExtensionStoreType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| SPCatalog | `0` | Especifica que el tipo de tienda es catálogo corporativo de SharePoint. |
| OMEX | `1` | Especifica que el tipo de tienda es Office.com. |
| SPApp | `2` | Especifica que el tipo de tienda es una aplicación web de SharePoint. |
| Exchange | `3` | Especifica que el tipo de almacén es un servidor Exchange. |
| FileSystem | `4` | Especifica que el tipo de almacén es un recurso compartido del sistema de archivos. |
| Registry | `5` | Especifica que el tipo de almacén es el registro del sistema. |
| ExCatalog | `6` | Especifica que el tipo de tienda es Implementación centralizada a través de Exchange. |
| Default | `0` | Valor predeterminado. |

### Ejemplos

Muestra cómo agregar una extensión web a un documento.

```csharp
Document doc = new Document();

// Crea un panel de tareas con el complemento "MyScript", que será utilizado por el documento.
// luego establece su ubicación predeterminada.
TaskPane myScriptTaskPane = new TaskPane();
doc.WebExtensionTaskPanes.Add(myScriptTaskPane);
myScriptTaskPane.DockState = TaskPaneDockState.Right;
myScriptTaskPane.IsVisible = true;
myScriptTaskPane.Width = 300;
myScriptTaskPane.IsLocked = true;

// Si hay varios paneles de tareas en la misma ubicación de acoplamiento, podemos configurar este índice para organizarlos.
myScriptTaskPane.Row = 1;

// Cree un complemento llamado "Muestra de matemáticas MyScript", que se mostrará en el panel de tareas.
WebExtension webExtension = myScriptTaskPane.WebExtension;

// Establece los parámetros de referencia de la tienda de aplicaciones para nuestro complemento, como el ID.
webExtension.Reference.Id = "WA104380646";
webExtension.Reference.Version = "1.0.0.0";
webExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
webExtension.Reference.Store = CultureInfo.CurrentCulture.Name;
webExtension.Properties.Add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
webExtension.Bindings.Add(new WebExtensionBinding("MyScript", WebExtensionBindingType.Text, "104380646"));

// Permitir que el usuario interactúe con el complemento.
webExtension.IsFrozen = false;

// Podemos acceder a la extensión web en Microsoft Word vía Developer -> Complementos.
doc.Save(ArtifactsDir + "Document.WebExtension.docx");

// Elimina todos los paneles de tareas de extensiones web a la vez, así.
doc.WebExtensionTaskPanes.Clear();

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Ver también

* espacio de nombres [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* asamblea [Aspose.Words](../../)


