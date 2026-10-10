---
title: "Aspose::Words::SaveFormat enum"
linktitle: "SaveFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::SaveFormat enum. Indica il formato in cui il documento viene salvato in C++."
type: docs
weight: 114000
url: /it/cpp/aspose.words/saveformat/
---
## SaveFormat enum


Indica il formato in cui il documento viene salvato.

```cpp
enum class SaveFormat
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Sconosciuto | 0 | Predefinito, valore non valido per il formato file. |
| Doc | 10 | Salva il documento nel formato Microsoft Word 97 - 2007 [Document](../document/). |
| Dot | 11 | Salva il documento nel formato Microsoft Word 97 - 2007 Template. |
| Docx | 20 | Salva il documento come un [Document](../document/) Office Open XML WordprocessingML (senza macro). |
| Docm | 21 | Salva il documento come un Office Open XML WordprocessingML abilitato alle macro [Document](../document/). |
| Dotx | 22 | Salva il documento come un modello Office Open XML WordprocessingML (senza macro). |
| Dotm | 23 | Salva il documento come un modello Office Open XML WordprocessingML abilitato alle macro. |
| FlatOpc | 24 | Salva il documento come un Office Open XML WordprocessingML memorizzato in un file XML piatto invece di un pacchetto ZIP. |
| FlatOpcMacroEnabled | 25 | Salva il documento come un Office Open XML WordprocessingML abilitato alle macro [Document](../document/) memorizzato in un file XML piatto invece di un pacchetto ZIP. |
| FlatOpcTemplate | 26 | Salva il documento come un modello Office Open XML WordprocessingML (senza macro) memorizzato in un file XML piatto invece di un pacchetto ZIP. |
| FlatOpcTemplateMacroEnabled | 27 | Salva il documento come un modello Office Open XML WordprocessingML abilitato alle macro memorizzato in un file XML piatto invece di un pacchetto ZIP. |
| Rtf | 30 | Salva il documento nel formato RTF. Tutti i caratteri superiori a 7 bit sono codificati come caratteri esadecimali o Unicode. |
| WordML | 31 | Salva il documento nel formato Microsoft Word 2003 WordprocessingML. |
| Pdf | 40 | Salva il documento come PDF (Adobe Portable [Document](../document/)) formato. |
| Xps | 41 | Salva il documento nel formato XPS (XML Paper Specification). |
| XamlFixed | 42 | Salva il documento nel formato Extensible Application [Markup](../../aspose.words.markup/) Language (XAML) come documento fisso. |
| Svg | 44 | Salva il documento nel formato Svg (Scalable Vector Graphics). |
| HtmlFixed | 45 | Salva il documento nel formato HTML usando elementi posizionati assolutamente. |
| OpenXps | 46 | Salva il documento nel formato OpenXPS (Ecma-388). |
| Ps | 47 | Salva il documento nel formato PS (PostScript). |
| Pcl | 48 | Salva il documento nel formato PCL (Printer Control Language). |
| Html | 50 | Salva il documento nel formato HTML. |
| Mhtml | 51 | Salva il documento nel formato MHTML (archivio web). |
| Epub | 52 | Salva il documento nel formato EPUB. |
| Azw3 | 53 | Salva il documento nel formato AZW3. |
| Mobi | 54 | Salva il documento nel formato MOBI. |
| Odt | 60 | Salva il documento come un ODF Text [Document](../document/). |
| Ott | 61 | Salva il documento come un ODF Text [Document](../document/) Template. |
| Testo | 70 | Salva il documento nel formato testo semplice. |
| XamlFlow | 71 | **Beta.** Salva il documento nel formato Extensible Application [Markup](../../aspose.words.markup/) Language (XAML) come documento a flusso. |
| XamlFlowPack | 72 | **Beta.** Salva il documento nel formato Extensible Application [Markup](../../aspose.words.markup/) Language (XAML) package come documento a flusso. |
| Markdown | 73 | Salva il documento nel formato Markdown. |
| Xlsx | 80 | Salva il documento come un Office Open XML SpreadsheetML [Document](../document/) (senza macro). |
| Docling | 81 | Salva il documento nel formato Docling JSON. |
| Tiff | 100 | Esegue il rendering di una o più pagine del documento e le salva in un file TIFF singolo o multipagina. |
| Png | 101 | Esegue il rendering di una pagina del documento e la salva come file PNG. |
| Bmp | 102 | Esegue il rendering di una pagina del documento e la salva come file BMP. |
| Emf | 103 | Esegue il rendering di una pagina del documento e la salva come file vettoriale EMF (Enhanced Meta File). |
| Jpeg | 104 | Esegue il rendering di una pagina del documento e la salva come file JPEG. |
| Gif | 105 | Esegue il rendering di una pagina del documento e la salva come file GIF. |
| Eps | 106 | Esegue il rendering di una pagina del documento e la salva come file EPS. |


## Esempi



Mostra come convertire da formato DOCX a HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToHtml.html", Aspose::Words::SaveFormat::Html);
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
