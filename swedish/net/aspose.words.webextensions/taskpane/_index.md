---
title: TaskPane Class
linktitle: TaskPane
articleTitle: TaskPane
second_title: Aspose.Words för .NET
description: Aspose.Words.WebExtensions.TaskPane klass. Representerar ett tilläggsaktivitetsfönsterobjekt i C#.
type: docs
weight: 6710
url: /sv/net/aspose.words.webextensions/taskpane/
---
## TaskPane class

Representerar ett tilläggsaktivitetsfönsterobjekt.

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
| [IsVisible](../../aspose.words.webextensions/taskpane/isvisible/) { get; set; } | Anger om aktivitetsfönstret visas som standard när dokumentet öppnas. |
| [Row](../../aspose.words.webextensions/taskpane/row/) { get; set; } | Anger indexet, uppräknat från utsidan till insidan, för den här aktivitetsrutan bland andra persisted uppgiftsrutor dockade på samma standardplats. |
| [WebExtension](../../aspose.words.webextensions/taskpane/webextension/) { get; } | Representerar ett webbtilläggsobjekt. |
| [Width](../../aspose.words.webextensions/taskpane/width/) { get; set; } | Anger standardbreddvärdet för den här uppgiftsrutans instans. |

## Exempel

Visar hur man lägger till ett webbtillägg till ett dokument.

```csharp
Document doc = new Document();

// Skapa aktivitetsfönster med "MyScript"-tillägget, som kommer att användas av dokumentet,
// ställ sedan in dess standardplats.
TaskPane myScriptTaskPane = new TaskPane();
doc.WebExtensionTaskPanes.Add(myScriptTaskPane);
myScriptTaskPane.DockState = TaskPaneDockState.Right;
myScriptTaskPane.IsVisible = true;
myScriptTaskPane.Width = 300;
myScriptTaskPane.IsLocked = true;

// Om det finns flera uppgiftsrutor på samma dockningsplats kan vi ställa in detta index för att ordna dem.
myScriptTaskPane.Row = 1;

// Skapa ett tillägg som heter "MyScript Math Sample", som aktivitetsfönstret kommer att visas i.
WebExtension webExtension = myScriptTaskPane.WebExtension;

// Ställ in referensparametrar för applikationsarkivet för vårt tillägg, till exempel ID.
webExtension.Reference.Id = "WA104380646";
webExtension.Reference.Version = "1.0.0.0";
webExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
webExtension.Reference.Store = CultureInfo.CurrentCulture.Name;
webExtension.Properties.Add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
webExtension.Bindings.Add(new WebExtensionBinding("MyScript", WebExtensionBindingType.Text, "104380646"));

// Tillåt användaren att interagera med tillägget.
webExtension.IsFrozen = false;

// Vi kan komma åt webbtillägget i Microsoft Word via utvecklare -> Tillägg.
doc.Save(ArtifactsDir + "Document.WebExtension.docx");

// Ta bort alla aktivitetsrutor för webbtillägg på en gång så här.
doc.WebExtensionTaskPanes.Clear();

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Se även

* namnutrymme [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* hopsättning [Aspose.Words](../../)
