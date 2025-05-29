---
title: WebExtensionStoreType Enum
linktitle: WebExtensionStoreType
articleTitle: WebExtensionStoreType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.WebExtensionStoreType, qui propose divers types de magasins d'extensions Web pour une intégration transparente et des fonctionnalités améliorées.
type: docs
weight: 7670
url: /fr/net/aspose.words.webextensions/webextensionstoretype/
---
## WebExtensionStoreType enumeration

Énumère les types disponibles d'un magasin d'extensions Web.

```csharp
public enum WebExtensionStoreType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| SPCatalog | `0` | Spécifie que le type de magasin est un catalogue d'entreprise SharePoint. |
| OMEX | `1` | Spécifie que le type de magasin est Office.com. |
| SPApp | `2` | Spécifie que le type de magasin est une application Web SharePoint. |
| Exchange | `3` | Spécifie que le type de magasin est un serveur Exchange. |
| FileSystem | `4` | Spécifie que le type de magasin est un partage de système de fichiers. |
| Registry | `5` | Spécifie que le type de magasin est le registre système. |
| ExCatalog | `6` | Spécifie que le type de magasin est Déploiement centralisé via Exchange. |
| Default | `0` | Valeur par défaut. |

## Exemples

Montre comment ajouter une extension Web à un document.

```csharp
Document doc = new Document();

// Créer un volet des tâches avec le complément « MyScript », qui sera utilisé par le document,
// puis définissez son emplacement par défaut.
TaskPane myScriptTaskPane = new TaskPane();
doc.WebExtensionTaskPanes.Add(myScriptTaskPane);
myScriptTaskPane.DockState = TaskPaneDockState.Right;
myScriptTaskPane.IsVisible = true;
myScriptTaskPane.Width = 300;
myScriptTaskPane.IsLocked = true;

// S'il existe plusieurs volets de tâches dans le même emplacement d'ancrage, nous pouvons définir cet index pour les organiser.
myScriptTaskPane.Row = 1;

// Créez un complément appelé « MyScript Math Sample », dans lequel le volet des tâches s'affichera.
WebExtension webExtension = myScriptTaskPane.WebExtension;

// Définissez les paramètres de référence de l'App Store pour notre complément, tels que l'ID.
webExtension.Reference.Id = "WA104380646";
webExtension.Reference.Version = "1.0.0.0";
webExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
webExtension.Reference.Store = CultureInfo.CurrentCulture.Name;
webExtension.Properties.Add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
webExtension.Bindings.Add(new WebExtensionBinding("MyScript", WebExtensionBindingType.Text, "104380646"));

// Autoriser l'utilisateur à interagir avec le complément.
webExtension.IsFrozen = false;

// Nous pouvons accéder à l'extension Web dans Microsoft Word via Développeur -> Modules complémentaires.
doc.Save(ArtifactsDir + "Document.WebExtension.docx");

// Supprimez tous les volets de tâches d'extension Web à la fois comme ceci.
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

### Voir également

* espace de noms [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* Assemblée [Aspose.Words](../../)
