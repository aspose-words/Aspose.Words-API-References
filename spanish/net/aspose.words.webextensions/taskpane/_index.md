---
title: TaskPane Class
linktitle: TaskPane
articleTitle: TaskPane
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.WebExtensions.TaskPane, su clave para crear potentes paneles de tareas complementarios para mejorar la edición y la productividad de documentos.
type: docs
weight: 7560
url: /es/net/aspose.words.webextensions/taskpane/
---
## TaskPane class

Representa un objeto del panel de tareas del complemento.

Para obtener más información, visite el[Trabajar con complementos de Office](https://docs.aspose.com/words/net/work-with-office-add-ins/) Artículo de documentación.

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
| [Row](../../aspose.words.webextensions/taskpane/row/) { get; set; } | Especifica el índice, enumerando desde afuera hacia adentro, de este panel de tareas entre otros paneles de tareas persistentes acoplados en la misma ubicación predeterminada. |
| [WebExtension](../../aspose.words.webextensions/taskpane/webextension/) { get; } | Representa un objeto de extensión web. |
| [Width](../../aspose.words.webextensions/taskpane/width/) { get; set; } | Especifica el valor de ancho predeterminado para esta instancia del panel de tareas. |

## Ejemplos

Muestra cómo agregar una extensión web a un documento.

```csharp
Document doc = new Document();

// Crear un panel de tareas con el complemento "MyScript", que será utilizado por el documento,
// luego establece su ubicación predeterminada.
TaskPane myScriptTaskPane = new TaskPane();
doc.WebExtensionTaskPanes.Add(myScriptTaskPane);
myScriptTaskPane.DockState = TaskPaneDockState.Right;
myScriptTaskPane.IsVisible = true;
myScriptTaskPane.Width = 300;
myScriptTaskPane.IsLocked = true;

// Si hay varios paneles de tareas en la misma ubicación de acoplamiento, podemos configurar este índice para organizarlos.
myScriptTaskPane.Row = 1;

// Cree un complemento llamado "MyScript Math Sample", que se mostrará en el panel de tareas.
WebExtension webExtension = myScriptTaskPane.WebExtension;

// Establezca los parámetros de referencia de la tienda de aplicaciones para nuestro complemento, como el ID.
webExtension.Reference.Id = "WA104380646";
webExtension.Reference.Version = "1.0.0.0";
webExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
webExtension.Reference.Store = CultureInfo.CurrentCulture.Name;
webExtension.Properties.Add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
webExtension.Bindings.Add(new WebExtensionBinding("MyScript", WebExtensionBindingType.Text, "104380646"));

// Permitir que el usuario interactúe con el complemento.
webExtension.IsFrozen = false;

//Podemos acceder a la extensión web en Microsoft Word a través de Desarrollador -> Complementos.
doc.Save(ArtifactsDir + "Document.WebExtension.docx");

//Elimine todos los paneles de tareas de extensión web a la vez de esta manera.
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

### Ver también

* espacio de nombres [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* asamblea [Aspose.Words](../../)
