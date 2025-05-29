---
title: Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words für .NET
description: Erstellen Sie mühelos leere Word-Dokumente mit unserem benutzerfreundlichen Dokumentkonfigurator. Optimieren Sie Ihren Schreibprozess noch heute!
type: docs
weight: 10
url: /de/net/aspose.words/document/document/
---
## Document() {#constructor}

Erstellt ein leeres Word-Dokument.

```csharp
public Document()
```

## Bemerkungen

Ein leeres Dokument wird aus Ressourcen abgerufen, und standardmäßig sieht das resultierende Dokument eher aus wie erstellt vonWord2007. Dieses leere Dokument enthält eine Tabelle mit Standardschriftarten, minimale Standardstile und latente Stile.

[`OptimizeFor`](../../../aspose.words.settings/compatibilityoptions/optimizefor/) Die Methode kann verwendet werden, um den Dokumentinhalt sowie das Standardverhalten von Aspose.Words für eine bestimmte Version von MS Word zu optimieren.

Das Dokumentpapierformat ist standardmäßig Letter. Wenn Sie die Seiteneinrichtung ändern möchten, verwenden Sie [`PageSetup`](../../section/pagesetup/).

Nach der Erstellung können Sie[`DocumentBuilder`](../../documentbuilder/) um Dokumentinhalte einfach hinzuzufügen.

## Beispiele

Zeigt, wie ein Textlauf mithilfe seiner Schriftarteigenschaft formatiert wird.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

Zeigt, wie man ein einfaches Dokument erstellt.

```csharp
Document doc = new Document();

// Neue Dokumentobjekte werden standardmäßig mit dem minimalen Satz an Knoten geliefert
// erforderlich, um mit dem Hinzufügen von Inhalten wie Text und Formen zu beginnen: ein Abschnitt, ein Textkörper und ein Absatz.
doc.AppendChild(new Section(doc))
    .AppendChild(new Body(doc))
    .AppendChild(new Paragraph(doc))
    .AppendChild(new Run(doc, "Hello world!"));
```

Zeigt, wie Dokumente erstellt und geladen werden.

```csharp
// Es gibt zwei Möglichkeiten, mit Aspose.Words ein Dokumentobjekt zu erstellen.
// 1 - Erstellen Sie ein leeres Dokument:
Document doc = new Document();

// Neue Dokumentobjekte werden standardmäßig mit dem minimalen Satz an Knoten geliefert
// erforderlich, um mit dem Hinzufügen von Inhalten wie Text und Formen zu beginnen: ein Abschnitt, ein Textkörper und ein Absatz.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - Laden Sie ein Dokument, das im lokalen Dateisystem vorhanden ist:
doc = new Document(MyDir + "Document.docx");

// Geladene Dokumente haben Inhalte, auf die wir zugreifen und die wir bearbeiten können.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// Einige Vorgänge, die während des Ladens ausgeführt werden müssen, z. B. die Verwendung eines Kennworts zum Entschlüsseln eines Dokuments,
// kann durch Übergeben eines LoadOptions-Objekts beim Laden des Dokuments erfolgen.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## Document(*string*) {#constructor_3}

Öffnet ein vorhandenes Dokument aus einer Datei. Das Dateiformat wird automatisch erkannt.

```csharp
public Document(string fileName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Dateiname des zu öffnenden Dokuments. |

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Das Dokumentformat wird nicht erkannt oder nicht unterstützt. |
| [FileCorruptedException](../../filecorruptedexception/) | Das Dokument scheint beschädigt zu sein und kann nicht geladen werden. |
| Exception | Es liegt ein Problem mit dem Dokument vor und sollte den Entwicklern von Aspose.Words gemeldet werden. |
| IOException | Es liegt eine Eingabe-/Ausgabeausnahme vor. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Das Dokument ist verschlüsselt und erfordert zum Öffnen ein Kennwort, Sie haben jedoch ein falsches Kennwort eingegeben. |
| ArgumentException | Der Name der Datei darf nicht null oder eine leere Zeichenfolge sein. |

## Beispiele

Zeigt, wie man ein Dokument öffnet und in das PDF-Format konvertiert.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToPdf.pdf");
```

Zeigt, wie man eine PDF-Datei in eine DOCX-Datei konvertiert.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

// Laden Sie das gerade gespeicherte PDF-Dokument und konvertieren Sie es in .docx.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.docx");
```

Zeigt, wie eine PDF-Datei geladen wird.

```csharp
Document doc = new Aspose.Words.Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

// Nachfolgend finden Sie zwei Möglichkeiten zum Laden von PDF-Dokumenten mit Aspose-Produkten.
// 1 – Als Aspose.Words-Dokument laden:
Document asposeWordsDoc = new Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

Assert.AreEqual("Hello world!", asposeWordsDoc.GetText().Trim());

// 2 – Als Aspose.Pdf-Dokument laden:
Aspose.Pdf.Document asposePdfDoc = new Aspose.Pdf.Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

TextFragmentAbsorber textFragmentAbsorber = new TextFragmentAbsorber();
asposePdfDoc.Pages.Accept(textFragmentAbsorber);

Assert.AreEqual("Hello world!", textFragmentAbsorber.Text.Trim());
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## Document(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_4}

Öffnet ein vorhandenes Dokument aus einer Datei. Ermöglicht die Angabe zusätzlicher Optionen wie z. B. eines Verschlüsselungskennworts.

```csharp
public Document(string fileName, LoadOptions loadOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Dateiname des zu öffnenden Dokuments. |
| loadOptions | LoadOptions | Zusätzliche Optionen beim Laden eines Dokuments. Kann sein`null`. |

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Das Dokumentformat wird nicht erkannt oder nicht unterstützt. |
| [FileCorruptedException](../../filecorruptedexception/) | Das Dokument scheint beschädigt zu sein und kann nicht geladen werden. |
| Exception | Es liegt ein Problem mit dem Dokument vor und sollte den Entwicklern von Aspose.Words gemeldet werden. |
| IOException | Es liegt eine Eingabe-/Ausgabeausnahme vor. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Das Dokument ist verschlüsselt und erfordert zum Öffnen ein Kennwort, Sie haben jedoch ein falsches Kennwort eingegeben. |
| ArgumentException | Der Name der Datei darf nicht null oder eine leere Zeichenfolge sein. |

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

Zeigt, wie Dokumente erstellt und geladen werden.

```csharp
// Es gibt zwei Möglichkeiten, mit Aspose.Words ein Dokumentobjekt zu erstellen.
// 1 - Erstellen Sie ein leeres Dokument:
Document doc = new Document();

// Neue Dokumentobjekte werden standardmäßig mit dem minimalen Satz an Knoten geliefert
// erforderlich, um mit dem Hinzufügen von Inhalten wie Text und Formen zu beginnen: ein Abschnitt, ein Textkörper und ein Absatz.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - Laden Sie ein Dokument, das im lokalen Dateisystem vorhanden ist:
doc = new Document(MyDir + "Document.docx");

// Geladene Dokumente haben Inhalte, auf die wir zugreifen und die wir bearbeiten können.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// Einige Vorgänge, die während des Ladens ausgeführt werden müssen, z. B. die Verwendung eines Kennworts zum Entschlüsseln eines Dokuments,
// kann durch Übergeben eines LoadOptions-Objekts beim Laden des Dokuments erfolgen.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Siehe auch

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## Document(*Stream*) {#constructor_1}

Öffnet ein vorhandenes Dokument aus einem Stream. Das Dateiformat wird automatisch erkannt.

```csharp
public Document(Stream stream)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Streamen Sie, woher das Dokument geladen werden soll. |

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Das Dokumentformat wird nicht erkannt oder nicht unterstützt. |
| [FileCorruptedException](../../filecorruptedexception/) | Das Dokument scheint beschädigt zu sein und kann nicht geladen werden. |
| Exception | Es liegt ein Problem mit dem Dokument vor und sollte den Entwicklern von Aspose.Words gemeldet werden. |
| IOException | Es liegt eine Eingabe-/Ausgabeausnahme vor. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Das Dokument ist verschlüsselt und erfordert zum Öffnen ein Kennwort, Sie haben jedoch ein falsches Kennwort eingegeben. |
| ArgumentNullException | Der Stream darf nicht null sein. |
| NotSupportedException | Der Stream unterstützt weder Lesen noch Suchen. |
| ObjectDisposedException | Der Stream ist ein verworfenes Objekt. |

## Bemerkungen

Das Dokument muss am Anfang des Streams gespeichert werden. Der Stream muss eine zufällige Positionierung unterstützen.

## Beispiele

Zeigt, wie ein Dokument mithilfe eines Streams geladen wird.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.docx"))
{
    Document doc = new Document(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

Zeigt, wie ein Dokument von einer URL geladen wird.

```csharp
// Erstellen Sie eine URL, die auf ein Microsoft Word-Dokument verweist.
const string url = "https://filesamples.com/samples/document/docx/sample3.docx";

// Laden Sie das Dokument in ein Byte-Array herunter und laden Sie dieses Array dann mithilfe eines Speicherstreams in ein Dokument.
using (WebClient webClient = new WebClient())
{
    byte[] dataBytes = webClient.DownloadData(url);

    using (MemoryStream byteStream = new MemoryStream(dataBytes))
    {
        Document doc = new Document(byteStream);

        // In dieser Phase können wir den Inhalt des Dokuments lesen und bearbeiten und es dann im lokalen Dateisystem speichern.
        Assert.AreEqual("There are eight section headings in this document. At the beginning, \"Sample Document\" is a level 1 heading. " +
                        "The main section headings, such as \"Headings\" and \"Lists\" are level 2 headings. " +
                        "The Tables section contains two sub-headings, \"Simple Table\" and \"Complex Table,\" which are both level 3 headings.",
            doc.FirstSection.Body.Paragraphs[3].GetText().Trim());

        doc.Save(ArtifactsDir + "Document.LoadFromWeb.docx");
    }
}
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## Document(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_2}

Öffnet ein vorhandenes Dokument aus einem Stream. Ermöglicht die Angabe zusätzlicher Optionen, wie z. B. eines Verschlüsselungskennworts.

```csharp
public Document(Stream stream, LoadOptions loadOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Der Stream, aus dem das Dokument geladen werden soll. |
| loadOptions | LoadOptions | Zusätzliche Optionen beim Laden eines Dokuments. Kann sein`null`. |

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Das Dokumentformat wird nicht erkannt oder nicht unterstützt. |
| [FileCorruptedException](../../filecorruptedexception/) | Das Dokument scheint beschädigt zu sein und kann nicht geladen werden. |
| Exception | Es liegt ein Problem mit dem Dokument vor und sollte den Entwicklern von Aspose.Words gemeldet werden. |
| IOException | Es liegt eine Eingabe-/Ausgabeausnahme vor. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Das Dokument ist verschlüsselt und erfordert zum Öffnen ein Kennwort, Sie haben jedoch ein falsches Kennwort eingegeben. |
| ArgumentNullException | Der Stream darf nicht null sein. |
| NotSupportedException | Der Stream unterstützt weder Lesen noch Suchen. |
| ObjectDisposedException | Der Stream ist ein verworfenes Objekt. |

## Bemerkungen

Das Dokument muss am Anfang des Streams gespeichert werden. Der Stream muss eine zufällige Positionierung unterstützen.

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

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
