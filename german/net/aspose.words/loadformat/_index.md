---
title: LoadFormat Enum
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.LoadFormat, die Dokumentformate für nahtloses Laden und verbesserte Kompatibilität in Ihren Anwendungen definiert.
type: docs
weight: 4000
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
| MsWorks | `8` | Microsoft Works 8-Dokument. |
| Doc | `10` | Microsoft Word 95- oder Word 97 – 2003-Dokument. |
| Dot | `11` | Microsoft Word 95 oder Word 97 – 2003 Vorlage. |
| DocPreWord60 | `12` | Das Dokument liegt im Format vor Word 95 vor. Aspose.Words unterstützt das Laden solcher Dokumente derzeit nicht. |
| Docx | `20` | Office Open XML WordprocessingML-Dokument (ohne Makros). |
| Docm | `21` | Office Open XML WordprocessingML-Makro-fähiges Dokument. |
| Dotx | `22` | Office Open XML WordprocessingML-Vorlage (ohne Makros). |
| Dotm | `23` | Office Open XML WordprocessingML-Vorlage mit Makros. |
| FlatOpc | `24` | Office Open XML WordprocessingML in einer flachen XML-Datei statt in einem ZIP-Paket gespeichert. |
| FlatOpcMacroEnabled | `25` | Office Open XML WordprocessingML-Makro-fähiges Dokument, gespeichert in einer flachen XML-Datei statt in einem ZIP-Paket. |
| FlatOpcTemplate | `26` | Office Open XML WordprocessingML-Vorlage (ohne Makros), gespeichert in einer flachen XML-Datei statt in einem ZIP-Paket. |
| FlatOpcTemplateMacroEnabled | `27` | Office Open XML WordprocessingML-Makro-fähige Vorlage, gespeichert in einer flachen XML-Datei statt in einem ZIP-Paket. |
| Rtf | `30` | RTF-Format. |
| WordML | `31` | Microsoft Word 2003 WordprocessingML-Format. |
| Html | `50` | HTML-Format. |
| Mhtml | `51` | MHTML-Format (Webarchiv). |
| Mobi | `52` | MOBI-Format. Wird vom MobiPocket Reader und Amazon Kindle Readern verwendet. |
| Chm | `53` | CHM-Format (kompilierte HTML-Hilfe). |
| Azw3 | `54` | AZW3-Format. Wird von Amazon Kindle-Lesegeräten verwendet. |
| Epub | `55` | EPUB-Format. |
| Odt | `60` | ODF-Textdokument. |
| Ott | `61` | ODF-Textdokumentvorlage. |
| Text | `62` | Klartext. |
| Markdown | `63` | Markdown-Textdokument. |
| Pdf | `64` | PDF-Dokument. |
| Xml | `65` | XML-Dokument. |
| Unknown | `255` | Unbekanntes Format, kann nicht von Aspose.Words geladen werden. |

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

Zeigt, wie die FileFormatUtil-Methoden zum Erkennen des Formats eines Dokuments verwendet werden.

```csharp
// Laden Sie ein Dokument aus einer Datei, der eine Dateierweiterung fehlt, und ermitteln Sie dann das Dateiformat.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Unten sind zwei Methoden zum Konvertieren eines LoadFormats in das entsprechende SaveFormat.
    // 1 – Holen Sie sich die Dateierweiterungszeichenfolge für das LoadFormat und dann das entsprechende SaveFormat aus dieser Zeichenfolge:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Konvertieren Sie das LoadFormat direkt in sein SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Laden Sie ein Dokument aus dem Stream und speichern Sie es dann mit der automatisch erkannten Dateierweiterung.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
