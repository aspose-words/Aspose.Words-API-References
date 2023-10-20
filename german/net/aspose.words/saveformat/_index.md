---
title: SaveFormat Enum
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words für .NET
description: Aspose.Words.SaveFormat opsomming. Gibt das Format an in dem das Dokument gespeichert ist in C#.
type: docs
weight: 4840
url: /de/net/aspose.words/saveformat/
---
## SaveFormat enumeration

Gibt das Format an, in dem das Dokument gespeichert ist.

```csharp
public enum SaveFormat
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Unknown | `0` | Standardwert, ungültiger Wert für Dateiformat. |
| Doc | `10` | Speichert das Dokument im Microsoft Word 97 - 2007-Dokumentformat. |
| Dot | `11` | Speichert das Dokument im Microsoft Word 97 - 2007-Vorlagenformat. |
| Docx | `20` | Speichert das Dokument als Office Open XML WordprocessingML-Dokument (ohne Makros). |
| Docm | `21` | Speichert das Dokument als Office Open XML WordprocessingML Macro-Enabled Document. |
| Dotx | `22` | Speichert das Dokument als Office Open XML WordprocessingML-Vorlage (ohne Makros). |
| Dotm | `23` | Speichert das Dokument als Office Open XML WordprocessingML-Makro-fähige Vorlage. |
| FlatOpc | `24` | Speichert das Dokument als Office Open XML WordprocessingML, gespeichert in einer flachen XML-Datei statt in einem ZIP-Paket. |
| FlatOpcMacroEnabled | `25` | Speichert das Dokument als Office Open XML WordprocessingML-Makro-fähiges Dokument, das in einer flachen XML-Datei statt in einem ZIP-Paket gespeichert wird. |
| FlatOpcTemplate | `26` | Speichert das Dokument als Office Open XML WordprocessingML-Vorlage (makrofrei), gespeichert in einer flachen XML-Datei statt in einem ZIP-Paket. |
| FlatOpcTemplateMacroEnabled | `27` | Speichert das Dokument als Office Open XML WordprocessingML-Makro-fähige Vorlage, die in einer flachen XML-Datei statt in einem ZIP-Paket gespeichert wird. |
| Rtf | `30` | Speichert das Dokument im RTF-Format. Alle Zeichen über 7 Bit werden als Hexadezimal- oder Unicode-Zeichen maskiert. |
| WordML | `31` | Speichert das Dokument im Microsoft Word 2003 WordprocessingML-Format. |
| Pdf | `40` | Speichert das Dokument im PDF-Format (Adobe Portable Document). |
| Xps | `41` | Speichert das Dokument im XPS-Format (XML Paper Specification). |
| XamlFixed | `42` | Speichert das Dokument im XAML-Format (Extensible Application Markup Language) als festes Dokument. |
| Svg | `44` | Speichert das Dokument im SVG-Format (Scalable Vector Graphics). |
| HtmlFixed | `45` | Speichert das Dokument im HTML-Format mit absolut positionierten Elementen |
| OpenXps | `46` | Speichert das Dokument im OpenXPS-Format (Ecma-388). |
| Ps | `47` | Speichert das Dokument im PS-Format (PostScript). |
| Pcl | `48` | Speichert das Dokument im PCL-Format (Printer Control Language). |
| Html | `50` | Speichert das Dokument im HTML-Format. |
| Mhtml | `51` | Speichert das Dokument im MHTML-Format (Webarchiv). |
| Epub | `52` | Speichert das Dokument im EPUB-Format. |
| Azw3 | `53` | Speichert das Dokument im AZW3-Format. |
| Mobi | `54` | Speichert das Dokument im MOBI-Format. |
| Odt | `60` | Speichert das Dokument als ODF-Textdokument. |
| Ott | `61` | Speichert das Dokument als ODF-Textdokumentvorlage. |
| Text | `70` | Speichert das Dokument im Nur-Text-Format. |
| XamlFlow | `71` | **Beta.** Speichert das Dokument im XAML-Format (Extensible Application Markup Language) als Flow-Dokument. |
| XamlFlowPack | `72` | **Beta.** Speichert das Dokument im XAML-Paketformat (Extensible Application Markup Language) als Flow-Dokument. |
| Markdown | `73` | Speichert das Dokument im Markdown-Format. |
| Xlsx | `80` | Speichert das Dokument als Office Open XML SpreadsheetML-Dokument (ohne Makros). |
| Tiff | `100` | Rendert eine oder mehrere Seiten des Dokuments und speichert sie in einer ein- oder mehrseitigen TIFF-Datei. |
| Png | `101` | Rendert eine Seite des Dokuments und speichert sie als PNG-Datei. |
| Bmp | `102` | Rendert eine Seite des Dokuments und speichert sie als BMP-Datei. |
| Emf | `103` | Rendert eine Seite des Dokuments und speichert sie als Vektor-EMF-Datei (Enhanced Meta File). |
| Jpeg | `104` | Rendert eine Seite des Dokuments und speichert sie als JPEG-Datei. |
| Gif | `105` | Rendert eine Seite des Dokuments und speichert sie als GIF-Datei. |
| Eps | `106` | Rendert eine Seite des Dokuments und speichert sie als EPS-Datei. |

## Beispiele

Zeigt, wie man vom DOCX- in das HTML-Format konvertiert.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToHtml.html", SaveFormat.Html);
```

### Siehe auch

* method [Save](../document/save/)
* class [SaveOptions](../../aspose.words.saving/saveoptions/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
