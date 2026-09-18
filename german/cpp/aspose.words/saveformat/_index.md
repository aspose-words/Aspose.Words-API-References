---
title: "Aspose::Words::SaveFormat enum"
linktitle: "SaveFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::SaveFormat enum. Gibt das Format an, in dem das Dokument in C++ gespeichert wird."
type: docs
weight: 114000
url: /de/cpp/aspose.words/saveformat/
---
## SaveFormat enum


Gibt das Format an, in dem das Dokument gespeichert wird.

```cpp
enum class SaveFormat
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Unbekannt | 0 | Standard, ungültiger Wert für das Dateiformat. |
| Doc | 10 | Speichert das Dokument im Microsoft Word 97 - 2007 [Document](../document/) Format. |
| Dot | 11 | Speichert das Dokument im Microsoft Word 97 - 2007 Vorlagenformat. |
| Docx | 20 | Speichert das Dokument als ein Office Open XML WordprocessingML [Document](../document/) (makrofrei). |
| Docm | 21 | Speichert das Dokument als ein Office Open XML WordprocessingML Makro-aktiviertes [Document](../document/). |
| Dotx | 22 | Speichert das Dokument als ein Office Open XML WordprocessingML Vorlagenformat (makrofrei). |
| Dotm | 23 | Speichert das Dokument als ein Office Open XML WordprocessingML Makro-aktiviertes Vorlagenformat. |
| FlatOpc | 24 | Speichert das Dokument als ein Office Open XML WordprocessingML, das in einer flachen XML-Datei anstelle eines ZIP-Pakets gespeichert wird. |
| FlatOpcMacroEnabled | 25 | Speichert das Dokument als ein Office Open XML WordprocessingML Makro-aktiviertes [Document](../document/), das in einer flachen XML-Datei anstelle eines ZIP-Pakets gespeichert wird. |
| FlatOpcTemplate | 26 | Speichert das Dokument als ein Office Open XML WordprocessingML Vorlagenformat (makrofrei), das in einer flachen XML-Datei anstelle eines ZIP-Pakets gespeichert wird. |
| FlatOpcTemplateMacroEnabled | 27 | Speichert das Dokument als ein Office Open XML WordprocessingML Makro-aktiviertes Vorlagenformat, das in einer flachen XML-Datei anstelle eines ZIP-Pakets gespeichert wird. |
| Rtf | 30 | Speichert das Dokument im RTF-Format. Alle Zeichen über 7 Bit werden als hexadezimale oder Unicode-Zeichen kodiert. |
| WordML | 31 | Speichert das Dokument im Microsoft Word 2003 WordprocessingML-Format. |
| Pdf | 40 | Speichert das Dokument im PDF (Adobe Portable [Dokument](../document/)) Format. |
| Xps | 41 | Speichert das Dokument im XPS (XML Paper Specification)-Format. |
| XamlFixed | 42 | Speichert das Dokument im Extensible Application [Markup](../../aspose.words.markup/) Language (XAML)-Format als ein festes Dokument. |
| Svg | 44 | Speichert das Dokument im Svg (Scalable Vector Graphics)-Format. |
| HtmlFixed | 45 | Speichert das Dokument im HTML-Format unter Verwendung absolut positionierter Elemente. |
| OpenXps | 46 | Speichert das Dokument im OpenXPS (Ecma-388)-Format. |
| Ps | 47 | Speichert das Dokument im PS (PostScript)-Format. |
| Pcl | 48 | Speichert das Dokument im PCL (Printer Control Language)-Format. |
| Html | 50 | Speichert das Dokument im HTML-Format. |
| Mhtml | 51 | Speichert das Dokument im MHTML (Web-Archiv)-Format. |
| Epub | 52 | Speichert das Dokument im EPUB-Format. |
| Azw3 | 53 | Speichert das Dokument im AZW3-Format. |
| Mobi | 54 | Speichert das Dokument im MOBI-Format. |
| Odt | 60 | Speichert das Dokument als ODF-Text [Dokument](../document/). |
| Ott | 61 | Speichert das Dokument als ODF-Text [Dokument](../document/) Vorlage. |
| Text | 70 | Speichert das Dokument im Nur-Text-Format. |
| XamlFlow | 71 | **Beta.** Speichert das Dokument im Extensible Application [Markup](../../aspose.words.markup/) Language (XAML)-Format als Flussdokument. |
| XamlFlowPack | 72 | **Beta.** Speichert das Dokument im Extensible Application [Markup](../../aspose.words.markup/) Language (XAML)-Paketformat als Flussdokument. |
| Markdown | 73 | Speichert das Dokument im Markdown-Format. |
| Xlsx | 80 | Speichert das Dokument als Office Open XML SpreadsheetML [Document](../document/) (makrofrei). |
| Docling | 81 | Speichert das Dokument im Docling JSON-Format. |
| Tiff | 100 | Rendert eine Seite oder mehrere Seiten des Dokuments und speichert sie in einer einzelnen oder mehrseitigen TIFF-Datei. |
| Png | 101 | Rendert eine Seite des Dokuments und speichert sie als PNG-Datei. |
| Bmp | 102 | Rendert eine Seite des Dokuments und speichert sie als BMP-Datei. |
| Emf | 103 | Rendert eine Seite des Dokuments und speichert sie als Vektor‑EMF (Enhanced Meta File)-Datei. |
| Jpeg | 104 | Rendert eine Seite des Dokuments und speichert sie als JPEG-Datei. |
| Gif | 105 | Rendert eine Seite des Dokuments und speichert sie als GIF-Datei. |
| Eps | 106 | Rendert eine Seite des Dokuments und speichert sie als EPS-Datei. |


## Beispiele



Zeigt, wie man von DOCX nach HTML konvertiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToHtml.html", Aspose::Words::SaveFormat::Html);
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
