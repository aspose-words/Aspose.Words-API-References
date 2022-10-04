---
title: LoadFormat
second_title: Aspose.Words für .NET-API-Referenz
description: Gibt das Format des zu ladenden Dokuments an.
type: docs
weight: 3350
url: /de/net/aspose.words/loadformat/
---
## LoadFormat enumeration

Gibt das Format des zu ladenden Dokuments an.

```csharp
public enum LoadFormat
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Auto | `0` | Weist Aspose.Words an, das Format automatisch zu erkennen. |
| Doc | `10` | Microsoft Word 95 oder Word 97 - 2003 Dokument. |
| Dot | `11` | Vorlage für Microsoft Word 95 oder Word 97 - 2003. |
| DocPreWord60 | `12` | Das Dokument ist im Format vor Word 95. Aspose.Words unterstützt derzeit das Laden solcher Dokumente nicht. |
| Docx | `20` | Office Open XML WordprocessingML-Dokument (makrofrei). |
| Docm | `21` | Office Open XML WordprocessingML-Dokument mit Makros. |
| Dotx | `22` | Office Open XML WordprocessingML-Vorlage (makrofrei). |
| Dotm | `23` | Vorlage mit Makros für Office Open XML WordprocessingML. |
| FlatOpc | `24` | Office Open XML WordprocessingML gespeichert in einer flachen XML-Datei anstelle eines ZIP-Pakets. |
| FlatOpcMacroEnabled | `25` | Office Open XML WordprocessingML-Dokument mit Makros, das in einer flachen XML-Datei statt in einem ZIP-Paket gespeichert ist. |
| FlatOpcTemplate | `26` | Office Open XML WordprocessingML-Vorlage (makrofrei), gespeichert in einer flachen XML-Datei anstelle eines ZIP-Pakets. |
| FlatOpcTemplateMacroEnabled | `27` | Makrofähige Vorlage für Office Open XML WordprocessingML, gespeichert in einer flachen XML-Datei anstelle eines ZIP-Pakets. |
| Rtf | `30` | RTF-Format. |
| WordML | `31` | Microsoft Word 2003 WordprocessingML-Format. |
| Html | `50` | HTML-Format. |
| Mhtml | `51` | MHTML-Format (Webarchiv). |
| Mobi | `52` | MOBI-Format. Wird von MobiPocket-Lesegeräten und Amazon Kindle-Lesegeräten verwendet. |
| Chm | `53` | CHM-Format (kompilierte HTML-Hilfe). |
| Azw3 | `54` | AZW3-Format. Wird von Amazon Kindle-Lesegeräten verwendet. |
| Epub | `55` | EPUB-Format. |
| Odt | `60` | ODF-Textdokument. |
| Ott | `61` | ODF-Textdokumentvorlage. |
| Text | `62` | Einfacher Text. |
| Markdown | `63` | Markdown-Textdokument. |
| Pdf | `64` | Pdf-Dokument. |
| Xml | `65` | XML-Dokument. |
| Unknown | `255` | Unbekanntes Format, kann nicht von Aspose.Words geladen werden. |

### Beispiele

Zeigt, wie eine Webseite als .docx-Datei gespeichert wird.

```csharp
const string url = "http://www.aspose.com/";

using (WebClient client = new WebClient()) 
{ 
    using (MemoryStream stream = new MemoryStream(client.DownloadData(url)))
    {
        // Die URL wird erneut als baseUri verwendet, um sicherzustellen, dass alle relativen Bildpfade korrekt abgerufen werden.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // Laden Sie das HTML-Dokument aus dem Stream und übergeben Sie das LoadOptions-Objekt.
        Document doc = new Document(stream, options);

        // An dieser Stelle können wir den Inhalt des Dokuments lesen und bearbeiten und es dann im lokalen Dateisystem speichern.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

Zeigt, wie beim Öffnen eines HTML-Dokuments ein Basis-URI angegeben wird.

```csharp
// Angenommen, wir möchten ein .html-Dokument laden, das ein Bild enthält, das durch einen relativen URI verknüpft ist
// während sich das Bild an einem anderen Ort befindet. In diesem Fall müssen wir den relativen URI in einen absoluten auflösen.
 // Wir können einen Basis-URI mit einem HtmlLoadOptions-Objekt bereitstellen.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Während das Bild in der Eingabe-.html-Datei beschädigt war, half uns unsere benutzerdefinierte Basis-URI, den Link zu reparieren.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Dieses Ausgabedokument zeigt das fehlende Bild an.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

Zeigt, wie die FileFormatUtil-Methoden verwendet werden, um das Format eines Dokuments zu erkennen.

```csharp
// Laden Sie ein Dokument aus einer Datei, der eine Dateierweiterung fehlt, und erkennen Sie dann das Dateiformat.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Unten sind zwei Methoden zum Konvertieren eines LoadFormats in sein entsprechendes SaveFormat.
    // 1 - Holen Sie sich die Dateierweiterungszeichenfolge für das LoadFormat, dann erhalten Sie das entsprechende SaveFormat aus dieser Zeichenfolge:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Konvertiere das LoadFormat direkt in sein SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Laden Sie ein Dokument aus dem Stream und speichern Sie es dann in der automatisch erkannten Dateierweiterung.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
