---
title: WebExtension Class
linktitle: WebExtension
articleTitle: WebExtension
second_title: Aspose.Words für .NET
description: Aspose.Words.WebExtensions.WebExtension klas. Stellt ein Weberweiterungsobjekt dar in C#.
type: docs
weight: 6740
url: /de/net/aspose.words.webextensions/webextension/
---
## WebExtension class

Stellt ein Weberweiterungsobjekt dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten Sie mit Office-Add-Ins](https://docs.aspose.com/words/net/work-with-office-add-ins/) Dokumentationsartikel.

```csharp
public class WebExtension
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AlternateReferences](../../aspose.words.webextensions/webextension/alternatereferences/) { get; } | Gibt alternative Verweise auf eine Weberweiterung an. |
| [Bindings](../../aspose.words.webextensions/webextension/bindings/) { get; } | Gibt eine Liste von Weberweiterungsbindungen an. |
| [Id](../../aspose.words.webextensions/webextension/id/) { get; set; } | Identifiziert eindeutig die Web-Erweiterungsinstanz im aktuellen Dokument. |
| [IsFrozen](../../aspose.words.webextensions/webextension/isfrozen/) { get; set; } | Gibt an, ob der Benutzer mit der Weberweiterung interagieren kann oder nicht. |
| [Properties](../../aspose.words.webextensions/webextension/properties/) { get; } | Stellt eine Reihe benutzerdefinierter Eigenschaften der Weberweiterung dar. |
| [Reference](../../aspose.words.webextensions/webextension/reference/) { get; } | Gibt den primären Verweis auf eine Weberweiterung an. |

## Beispiele

Zeigt, wie man einem Dokument eine Weberweiterung hinzufügt.

```csharp
Document doc = new Document();

// Aufgabenbereich mit „MyScript“-Add-in erstellen, der vom Dokument verwendet wird,
// dann den Standardspeicherort festlegen.
TaskPane myScriptTaskPane = new TaskPane();
doc.WebExtensionTaskPanes.Add(myScriptTaskPane);
myScriptTaskPane.DockState = TaskPaneDockState.Right;
myScriptTaskPane.IsVisible = true;
myScriptTaskPane.Width = 300;
myScriptTaskPane.IsLocked = true;

// Wenn sich mehrere Aufgabenbereiche am selben Andockort befinden, können wir diesen Index festlegen, um sie anzuordnen.
myScriptTaskPane.Row = 1;

// Erstellen Sie ein Add-In mit dem Namen „MyScript Math Sample“, in dem der Aufgabenbereich angezeigt wird.
WebExtension webExtension = myScriptTaskPane.WebExtension;

// Legen Sie Referenzparameter für den Anwendungsspeicher für unser Add-In fest, z. B. die ID.
webExtension.Reference.Id = "WA104380646";
webExtension.Reference.Version = "1.0.0.0";
webExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
webExtension.Reference.Store = CultureInfo.CurrentCulture.Name;
webExtension.Properties.Add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
webExtension.Bindings.Add(new WebExtensionBinding("MyScript", WebExtensionBindingType.Text, "104380646"));

// Dem Benutzer erlauben, mit dem Add-In zu interagieren.
webExtension.IsFrozen = false;

// Wir können über Developer -> auf die Web-Erweiterung in Microsoft Word zugreifen. Add-Ins.
doc.Save(ArtifactsDir + "Document.WebExtension.docx");

// Entfernen Sie auf diese Weise alle Aufgabenbereiche der Weberweiterung auf einmal.
doc.WebExtensionTaskPanes.Clear();

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Siehe auch

* namensraum [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* Montage [Aspose.Words](../../)
