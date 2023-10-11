---
title: Class TaskPane
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.WebExtensions.TaskPane clase. Representa un objeto de panel de tareas complementario.
type: docs
weight: 6710
url: /es/net/aspose.words.webextensions/taskpane/
---
## TaskPane class

Representa un objeto de panel de tareas complementario.

Para obtener más información, visite el[Trabajar con complementos de Office](https://docs.aspose.com/words/net/work-with-office-add-ins/) artículo de documentación.

```csharp
public class TaskPane
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [TaskPane](taskpane/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DockState](../../aspose.words.webextensions/taskpane/dockstate/) { get; set; } | Especifica la última ubicación acoplada de este objeto del panel de tareas. |
| [IsLocked](../../aspose.words.webextensions/taskpane/islocked/) { get; set; } | Especifica si el panel de tareas está bloqueado en el documento en la interfaz de usuario y el usuario no puede cerrarlo. |
| [IsVisible](../../aspose.words.webextensions/taskpane/isvisible/) { get; set; } | Especifica si el panel de tareas se muestra como visible de forma predeterminada cuando se abre el documento. |
| [Row](../../aspose.words.webextensions/taskpane/row/) { get; set; } | Especifica el índice, enumerado desde el exterior hacia el interior, de este panel de tareas entre otros paneles de tareas persistentes acoplados en la misma ubicación predeterminada. |
| [WebExtension](../../aspose.words.webextensions/taskpane/webextension/) { get; } | Representa un objeto de extensión web. |
| [Width](../../aspose.words.webextensions/taskpane/width/) { get; set; } | Especifica el valor de ancho predeterminado para esta instancia del panel de tareas. |

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


