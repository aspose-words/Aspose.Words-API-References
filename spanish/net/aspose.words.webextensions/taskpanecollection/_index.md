---
title: TaskPaneCollection Class
linktitle: TaskPaneCollection
articleTitle: TaskPaneCollection
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.WebExtensions.TaskPaneCollection, su solución para gestionar eficientemente objetos persistentes del panel de tareas. ¡Mejore sus aplicaciones web hoy mismo!
type: docs
weight: 7570
url: /es/net/aspose.words.webextensions/taskpanecollection/
---
## TaskPaneCollection class

Especifica una lista de objetos del panel de tareas persistentes.

Para obtener más información, visite el[Trabajar con complementos de Office](https://docs.aspose.com/words/net/work-with-office-add-ins/) Artículo de documentación.

```csharp
public class TaskPaneCollection : BaseWebExtensionCollection<TaskPane>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.webextensions/basewebextensioncollection-1/count/) { get; } |  |
| [Item](../../aspose.words.webextensions/basewebextensioncollection-1/item/) { get; set; } |  |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words.webextensions/basewebextensioncollection-1/add/)(*[TaskPane](../taskpane/)*) |  |
| [Clear](../../aspose.words.webextensions/basewebextensioncollection-1/clear/)() |  |
| [GetEnumerator](../../aspose.words.webextensions/basewebextensioncollection-1/getenumerator/)() |  |
| [Remove](../../aspose.words.webextensions/basewebextensioncollection-1/remove/)(*int*) |  |

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

* class [BaseWebExtensionCollection&lt;T&gt;](../basewebextensioncollection-1/)
* class [TaskPane](../taskpane/)
* espacio de nombres [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* asamblea [Aspose.Words](../../)
