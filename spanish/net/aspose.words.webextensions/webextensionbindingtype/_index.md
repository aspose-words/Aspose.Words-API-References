---
title: WebExtensionBindingType Enum
linktitle: WebExtensionBindingType
articleTitle: WebExtensionBindingType
second_title: Aspose.Words para .NET
description: Aspose.Words.WebExtensions.WebExtensionBindingType enumeración. Enumera los tipos de enlace disponibles entre una extensión web y los datos del documento en C#.
type: docs
weight: 6770
url: /es/net/aspose.words.webextensions/webextensionbindingtype/
---
## WebExtensionBindingType enumeration

Enumera los tipos de enlace disponibles entre una extensión web y los datos del documento.

```csharp
public enum WebExtensionBindingType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Matrix | `0` | Datos tabulares sin fila de encabezado. |
| Table | `1` | Datos tabulares con una fila de encabezado. |
| Text | `2` | Texto sin formato. |
| Default | `0` |  |

## Ejemplos

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
