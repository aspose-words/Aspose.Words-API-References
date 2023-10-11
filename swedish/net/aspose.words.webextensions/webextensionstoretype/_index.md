---
title: Enum WebExtensionStoreType
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.WebExtensions.WebExtensionStoreType uppräkning. Räknar upp tillgängliga typer av en webbtilläggsbutik.
type: docs
weight: 6820
url: /sv/net/aspose.words.webextensions/webextensionstoretype/
---
## WebExtensionStoreType enumeration

Räknar upp tillgängliga typer av en webbtilläggsbutik.

```csharp
public enum WebExtensionStoreType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| SPCatalog | `0` | Anger att butikstypen är SharePoint-företagskatalog. |
| OMEX | `1` | Anger att butikstypen är Office.com. |
| SPApp | `2` | Anger att butikstypen är en SharePoint-webbapplikation. |
| Exchange | `3` | Anger att butikstypen är en Exchange-server. |
| FileSystem | `4` | Anger att butikstypen är en filsystemsresurs. |
| Registry | `5` | Anger att butikstypen är systemregistret. |
| ExCatalog | `6` | Anger att butikstypen är centraliserad distribution via Exchange. |
| Default | `0` | Standardvärde. |

### Exempel

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


