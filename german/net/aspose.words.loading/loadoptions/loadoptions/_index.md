---
title: LoadOptions
linktitle: LoadOptions
articleTitle: LoadOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie den LoadOptions-Konstruktor, der für die mühelose Initialisierung einer neuen Instanz mit Standardwerten für optimale Leistung und Effizienz entwickelt wurde.
type: docs
weight: 10
url: /de/net/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions() {#constructor}

Initialisiert eine neue Instanz dieser Klasse mit Standardwerten.

```csharp
public LoadOptions()
```

## Beispiele

Zeigt, wie ein HTML-Dokument mit Bildern aus einem Stream unter Verwendung einer Basis-URI geöffnet wird.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Übergeben Sie die URI des Basisordners beim Laden
    // damit alle Bilder mit relativen URIs im HTML-Dokument gefunden werden können.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Überprüfen Sie, ob die erste Form des Dokuments ein gültiges Bild enthält.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

### Siehe auch

* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)

---

## LoadOptions(*string*) {#constructor_2}

Eine Verknüpfung zum Initialisieren einer neuen Instanz dieser Klasse mit dem angegebenen Kennwort zum Laden eines verschlüsselten Dokuments.

```csharp
public LoadOptions(string password)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| password | String | Das Passwort zum Öffnen eines verschlüsselten Dokuments. Kann sein`null` oder eine leere Zeichenfolge. |

## Beispiele

Zeigt, wie ein verschlüsseltes Microsoft Word-Dokument geladen wird.

```csharp
Document doc;

// Aspose.Words löst eine Ausnahme aus, wenn wir versuchen, ein verschlüsseltes Dokument ohne dessen Kennwort zu öffnen.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Beim Laden eines solchen Dokuments wird das Kennwort mithilfe eines LoadOptions-Objekts an den Konstruktor des Dokuments übergeben.
LoadOptions options = new LoadOptions("docPassword");

// Es gibt zwei Möglichkeiten, ein verschlüsseltes Dokument mit einem LoadOptions-Objekt zu laden.
// 1 - Laden Sie das Dokument aus dem lokalen Dateisystem nach Dateinamen:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Laden Sie das Dokument aus einem Stream:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

### Siehe auch

* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)

---

## LoadOptions(*[LoadFormat](../../../aspose.words/loadformat/), string, string*) {#constructor_1}

Eine Verknüpfung zum Initialisieren einer neuen Instanz dieser Klasse mit Eigenschaften, die auf die angegebenen Werte gesetzt sind.

```csharp
public LoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| loadFormat | LoadFormat | Das Format des zu ladenden Dokuments. |
| password | String | Das Passwort zum Öffnen eines verschlüsselten Dokuments. Kann sein`null` oder eine leere Zeichenfolge. |
| baseUri | String | Die Zeichenfolge, die zum Auflösen relativer URIs in absolute verwendet wird. Kann sein`null` oder eine leere Zeichenfolge. |

## Beispiele

Zeigt, wie eine Webseite als DOCX-Datei gespeichert wird.

```csharp
const string url = "https://products.aspose.com/words/";

using (WebClient client = new WebClient())
{
    var bytes = client.DownloadData(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // Die URL wird erneut als Basis-Uri verwendet, um sicherzustellen, dass alle relativen Bildpfade korrekt abgerufen werden.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // Laden Sie das HTML-Dokument aus dem Stream und übergeben Sie das LoadOptions-Objekt.
        Document doc = new Document(stream, options);

        // In dieser Phase können wir den Inhalt des Dokuments lesen und bearbeiten und es dann im lokalen Dateisystem speichern.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

Zeigt, wie beim Öffnen eines HTML-Dokuments eine Basis-URI angegeben wird.

```csharp
// Angenommen, wir möchten ein HTML-Dokument laden, das ein Bild enthält, das über eine relative URI verknüpft ist
// während sich das Bild an einem anderen Ort befindet. In diesem Fall müssen wir die relative URI in eine absolute auflösen.
    // Wir können eine Basis-URI mithilfe eines HtmlLoadOptions-Objekts bereitstellen.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Obwohl das Bild in der Eingabe-HTML beschädigt war, half uns unsere benutzerdefinierte Basis-URI, den Link zu reparieren.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Dieses Ausgabedokument zeigt das fehlende Bild an.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### Siehe auch

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
