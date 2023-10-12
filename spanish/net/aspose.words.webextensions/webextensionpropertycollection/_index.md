---
title: Class WebExtensionPropertyCollection
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.WebExtensions.WebExtensionPropertyCollection clase. Especifica un conjunto de propiedades personalizadas de extensión web.
type: docs
weight: 6790
url: /es/net/aspose.words.webextensions/webextensionpropertycollection/
---
## WebExtensionPropertyCollection class

Especifica un conjunto de propiedades personalizadas de extensión web.

Para obtener más información, visite el[Trabajar con complementos de Office](https://docs.aspose.com/words/net/work-with-office-add-ins/) artículo de documentación.

```csharp
public class WebExtensionPropertyCollection : BaseWebExtensionCollection<WebExtensionProperty>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.webextensions/basewebextensioncollection-1/count/) { get; } |  |
| [Item](../../aspose.words.webextensions/basewebextensioncollection-1/item/) { get; set; } |  |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words.webextensions/basewebextensioncollection-1/add/)(WebExtensionProperty) |  |
| [Clear](../../aspose.words.webextensions/basewebextensioncollection-1/clear/)() |  |
| [GetEnumerator](../../aspose.words.webextensions/basewebextensioncollection-1/getenumerator/)() |  |
| [Remove](../../aspose.words.webextensions/basewebextensioncollection-1/remove/)(int) |  |

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

* class [BaseWebExtensionCollection&lt;T&gt;](../basewebextensioncollection-1/)
* class [WebExtensionProperty](../webextensionproperty/)
* espacio de nombres [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* asamblea [Aspose.Words](../../)


