---
title: LoadOptions.LoadOptions
second_title: Aspose.Words für .NET-API-Referenz
description: LoadOptions constructeur. Initialisiert eine neue Instanz dieser Klasse mit Standardwerten.
type: docs
weight: 10
url: /de/net/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions() {#constructor}

Initialisiert eine neue Instanz dieser Klasse mit Standardwerten.

```csharp
public LoadOptions()
```

### Beispiele

Zeigt, wie man mithilfe eines Basis-URI ein HTML-Dokument mit Bildern aus einem Stream öffnet.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Beim Laden den URI des Basisordners übergeben
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
* namensraum [Aspose.Words.Loading](../../loadoptions/)
* Montage [Aspose.Words](../../../)

---

## LoadOptions(string) {#constructor_2}

Eine Verknüpfung zum Initialisieren einer neuen Instanz dieser Klasse mit dem angegebenen Kennwort, um ein verschlüsseltes Dokument zu laden.

```csharp
public LoadOptions(string password)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| password | String | Das Passwort zum Öffnen eines verschlüsselten Dokuments. Kann sein`Null` oder leere Zeichenfolge. |

### Beispiele

Zeigt, wie ein verschlüsseltes Microsoft Word-Dokument geladen wird.

```csharp
Document doc;

// Aspose.Words löst eine Ausnahme aus, wenn wir versuchen, ein verschlüsseltes Dokument ohne sein Passwort zu öffnen.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Beim Laden eines solchen Dokuments wird das Passwort mithilfe eines LoadOptions-Objekts an den Konstruktor des Dokuments übergeben.
LoadOptions options = new LoadOptions("docPassword");

// Es gibt zwei Möglichkeiten, ein verschlüsseltes Dokument mit einem LoadOptions-Objekt zu laden.
// 1 – Laden Sie das Dokument anhand des Dateinamens aus dem lokalen Dateisystem:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 – Laden Sie das Dokument aus einem Stream:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

### Siehe auch

* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../loadoptions/)
* Montage [Aspose.Words](../../../)

---

## LoadOptions(LoadFormat, string, string) {#constructor_1}

Eine Verknüpfung zum Initialisieren einer neuen Instanz dieser Klasse mit Eigenschaften, die auf die angegebenen Werte festgelegt sind.

```csharp
public LoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| loadFormat | LoadFormat | Das Format des zu ladenden Dokuments. |
| password | String | Das Passwort zum Öffnen eines verschlüsselten Dokuments. Kann sein`Null` oder leere Zeichenfolge. |
| baseUri | String | Die Zeichenfolge, die zum Auflösen relativer URIs in absolute verwendet wird. Kann sein`Null` oder leere Zeichenfolge. |

### Beispiele

Zeigt, wie eine Webseite als .docx-Datei gespeichert wird.

```csharp
const string url = "https://www.aspose.com/";

using (HttpClient client = new HttpClient()) 
{
    var bytes = await client.GetByteArrayAsync(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // Die URL wird erneut als BaseUri verwendet, um sicherzustellen, dass alle relativen Bildpfade korrekt abgerufen werden.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // Laden Sie das HTML-Dokument aus dem Stream und übergeben Sie das LoadOptions-Objekt.
        Document doc = new Document(stream, options);

        // In dieser Phase können wir den Inhalt des Dokuments lesen und bearbeiten und es dann im lokalen Dateisystem speichern.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

Zeigt, wie man beim Öffnen eines HTML-Dokuments einen Basis-URI angibt.

```csharp
// Angenommen, wir möchten ein HTML-Dokument laden, das ein durch einen relativen URI verknüpftes Bild enthält
// während sich das Bild an einem anderen Ort befindet. In diesem Fall müssen wir den relativen URI in einen absoluten auflösen.
 // Wir können einen Basis-URI mithilfe eines HtmlLoadOptions-Objekts bereitstellen.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Während das Bild in der Eingabe-HTML-Datei defekt war, half uns unser benutzerdefinierter Basis-URI, den Link zu reparieren.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Dieses Ausgabedokument zeigt das fehlende Bild an.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### Siehe auch

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../loadoptions/)
* Montage [Aspose.Words](../../../)


