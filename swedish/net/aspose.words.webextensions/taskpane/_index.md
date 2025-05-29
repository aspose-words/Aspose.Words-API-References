---
title: TaskPane Class
linktitle: TaskPane
articleTitle: TaskPane
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.WebExtensions.TaskPane, din nyckel till att skapa kraftfulla tilläggsfunktioner för förbättrad dokumentredigering och produktivitet.
type: docs
weight: 7560
url: /sv/net/aspose.words.webextensions/taskpane/
---
## TaskPane class

Representerar ett objekt i en tilläggsfunktion i aktivitetsfönstret.

För att lära dig mer, besök[Arbeta med Office-tillägg](https://docs.aspose.com/words/net/work-with-office-add-ins/) dokumentationsartikel.

```csharp
public class TaskPane
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [TaskPane](taskpane/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DockState](../../aspose.words.webextensions/taskpane/dockstate/) { get; set; } | Anger den senast dockade platsen för detta aktivitetsfönsterobjekt. |
| [IsLocked](../../aspose.words.webextensions/taskpane/islocked/) { get; set; } | Anger om aktivitetsfönstret är låst till dokumentet i användargränssnittet och inte kan stängas av användaren. |
| [IsVisible](../../aspose.words.webextensions/taskpane/isvisible/) { get; set; } | Anger om åtgärdsfönstret visas som synligt som standard när dokumentet öppnas. |
| [Row](../../aspose.words.webextensions/taskpane/row/) { get; set; } | Anger indexet, uppräknat från utsidan till insidan, för den här åtgärdsrutan bland andra bestående åtgärdsrutor som är dockade på samma standardplats. |
| [WebExtension](../../aspose.words.webextensions/taskpane/webextension/) { get; } | Representerar ett webbtilläggsobjekt. |
| [Width](../../aspose.words.webextensions/taskpane/width/) { get; set; } | Anger standardbredden för den här aktivitetsfönstrets instans. |

## Exempel

Visar hur man lägger till ett webbtillägg i ett dokument.

```csharp
Document doc = new Document();

// Skapa aktivitetsfönstret med tillägget "MyScript", som kommer att användas av dokumentet,
// ange sedan dess standardplats.
TaskPane myScriptTaskPane = new TaskPane();
doc.WebExtensionTaskPanes.Add(myScriptTaskPane);
myScriptTaskPane.DockState = TaskPaneDockState.Right;
myScriptTaskPane.IsVisible = true;
myScriptTaskPane.Width = 300;
myScriptTaskPane.IsLocked = true;

// Om det finns flera aktivitetsfönster på samma dockningsplats kan vi ställa in detta index för att ordna dem.
myScriptTaskPane.Row = 1;

// Skapa ett tillägg som heter "MyScript Math Sample", vilket visas i åtgärdsfönstret.
WebExtension webExtension = myScriptTaskPane.WebExtension;

// Ange referensparametrar för application store för vårt tillägg, till exempel ID.
webExtension.Reference.Id = "WA104380646";
webExtension.Reference.Version = "1.0.0.0";
webExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
webExtension.Reference.Store = CultureInfo.CurrentCulture.Name;
webExtension.Properties.Add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
webExtension.Bindings.Add(new WebExtensionBinding("MyScript", WebExtensionBindingType.Text, "104380646"));

// Tillåt användaren att interagera med tillägget.
webExtension.IsFrozen = false;

// Vi kan komma åt webbtillägget i Microsoft Word via Utvecklare -> Tillägg.
doc.Save(ArtifactsDir + "Document.WebExtension.docx");

// Ta bort alla aktivitetsfönster för webbtillägg på en gång så här.
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

### Se även

* namnutrymme [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* hopsättning [Aspose.Words](../../)
