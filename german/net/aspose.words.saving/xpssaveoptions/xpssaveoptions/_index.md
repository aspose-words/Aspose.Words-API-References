---
title: XpsSaveOptions.XpsSaveOptions
second_title: Aspose.Words für .NET-API-Referenz
description: XpsSaveOptions constructeur. Initialisiert eine neue Instanz dieser Klasse die zum Speichern eines Dokuments im verwendet werden kannXps format.
type: docs
weight: 10
url: /de/net/aspose.words.saving/xpssaveoptions/xpssaveoptions/
---
## XpsSaveOptions() {#constructor}

Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments im verwendet werden kannXps format.

```csharp
public XpsSaveOptions()
```

### Beispiele

Zeigt, wie man die Überschriftenebene einschränkt, die in der Gliederung eines gespeicherten XPS-Dokuments angezeigt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Überschriften einfügen, die als Inhaltsverzeichniseinträge der Ebenen 1, 2 und dann 3 dienen können.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Erstellen Sie ein „XpsSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .XPS konvertiert.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// Das ausgegebene XPS-Dokument enthält eine Gliederung, ein Inhaltsverzeichnis, das die Überschriften im Hauptteil des Dokuments auflistet.
// Durch Klicken auf einen Eintrag in dieser Gliederung gelangen wir zur Position der entsprechenden Überschrift.
// Setzen Sie die Eigenschaft „HeadingsOutlineLevels“ auf „2“, um alle Überschriften, deren Ebenen über 2 liegen, aus der Gliederung auszuschließen.
// Die letzten beiden Überschriften, die wir oben eingefügt haben, werden nicht angezeigt.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Siehe auch

* class [XpsSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../xpssaveoptions/)
* Montage [Aspose.Words](../../../)

---

## XpsSaveOptions(SaveFormat) {#constructor_1}

Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments im verwendet werden kannXps oderOpenXps format.

```csharp
public XpsSaveOptions(SaveFormat saveFormat)
```

### Beispiele

Zeigt, wie ein Dokument in Form einer Buchfalte im XPS-Format gespeichert wird.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Erstellen Sie ein „XpsSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .XPS konvertiert.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// Setzen Sie die Eigenschaft „UseBookFoldPrintingSettings“ auf „true“, um den Inhalt anzuordnen
// im Ausgabe-XPS auf eine Weise, die uns hilft, daraus eine Broschüre zu erstellen.
// Setzen Sie die Eigenschaft „UseBookFoldPrintingSettings“ auf „false“, um das XPS normal darzustellen.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// Wenn wir das Dokument als Broschüre rendern, müssen wir „MultiplePages“ festlegen.
// Eigenschaften der Seiteneinrichtungsobjekte aller Abschnitte zu „MultiplePagesType.BookFoldPrinting“.
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Sobald wir dieses Dokument gedruckt haben, können wir es durch Stapeln der Seiten in eine Broschüre umwandeln
// aus dem Drucker kommen und in der Mitte nach unten falten.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XpsSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../xpssaveoptions/)
* Montage [Aspose.Words](../../../)


