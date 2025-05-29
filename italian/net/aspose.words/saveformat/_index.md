---
title: SaveFormat Enum
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.SaveFormat per scegliere facilmente i formati di salvataggio dei documenti, migliorando la gestione dei file e la compatibilità per flussi di lavoro fluidi.
type: docs
weight: 5580
url: /it/net/aspose.words/saveformat/
---
## SaveFormat enumeration

Indica il formato in cui viene salvato il documento.

```csharp
public enum SaveFormat
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Unknown | `0` | Valore predefinito non valido per il formato file. |
| Doc | `10` | Salva il documento nel formato documento Microsoft Word 97 - 2007. |
| Dot | `11` | Salva il documento nel formato modello di Microsoft Word 97-2007. |
| Docx | `20` | Salva il documento come documento Office Open XML WordprocessingML (senza macro). |
| Docm | `21` | Salva il documento come documento con macro abilitate per Office Open XML WordprocessingML. |
| Dotx | `22` | Salva il documento come modello Office Open XML WordprocessingML (senza macro). |
| Dotm | `23` | Salva il documento come modello con macro abilitate per Office Open XML WordprocessingML. |
| FlatOpc | `24` | Salva il documento come un file Office Open XML WordprocessingML memorizzato in un file XML semplice anziché in un pacchetto ZIP. |
| FlatOpcMacroEnabled | `25` | Salva il documento come documento Office Open XML WordprocessingML Macro-Enabled, memorizzato in un file XML semplice anziché in un pacchetto ZIP. |
| FlatOpcTemplate | `26` | Salva il documento come modello Office Open XML WordprocessingML (senza macro) memorizzato in un file XML semplice anziché in un pacchetto ZIP. |
| FlatOpcTemplateMacroEnabled | `27` | Salva il documento come modello abilitato per macro di Office Open XML WordprocessingML, memorizzato in un file XML semplice anziché in un pacchetto ZIP. |
| Rtf | `30` | Salva il documento nel formato RTF. Tutti i caratteri superiori a 7 bit vengono codificati come caratteri esadecimali o Unicode. |
| WordML | `31` | Salva il documento nel formato WordprocessingML di Microsoft Word 2003. |
| Pdf | `40` | Salva il documento in formato PDF (Adobe Portable Document). |
| Xps | `41` | Salva il documento nel formato XPS (XML Paper Specification). |
| XamlFixed | `42` | Salva il documento nel formato Extensible Application Markup Language (XAML) come documento fisso. |
| Svg | `44` | Salva il documento nel formato Svg (Scalable Vector Graphics). |
| HtmlFixed | `45` | Salva il documento nel formato HTML utilizzando elementi posizionati in modo assoluto |
| OpenXps | `46` | Salva il documento nel formato OpenXPS (Ecma-388). |
| Ps | `47` | Salva il documento nel formato PS (PostScript). |
| Pcl | `48` | Salva il documento nel formato PCL (Printer Control Language). |
| Html | `50` | Salva il documento nel formato HTML. |
| Mhtml | `51` | Salva il documento nel formato MHTML (archivio Web). |
| Epub | `52` | Salva il documento nel formato EPUB. |
| Azw3 | `53` | Salva il documento nel formato AZW3. |
| Mobi | `54` | Salva il documento nel formato MOBI. |
| Odt | `60` | Salva il documento come documento di testo ODF. |
| Ott | `61` | Salva il documento come modello di documento di testo ODF. |
| Text | `70` | Salva il documento nel formato di testo normale. |
| XamlFlow | `71` | **Beta.** Salva il documento nel formato Extensible Application Markup Language (XAML) come documento di flusso. |
| XamlFlowPack | `72` | **Beta.** Salva il documento nel formato del pacchetto Extensible Application Markup Language (XAML) come documento di flusso. |
| Markdown | `73` | Salva il documento nel formato Markdown. |
| Xlsx | `80` | Salva il documento come documento Office Open XML SpreadsheetML (senza macro). |
| Tiff | `100` | Esegue il rendering di una o più pagine del documento e le salva in un file TIFF singolo o multipagina. |
| Png | `101` | Esegue il rendering di una pagina del documento e la salva come file PNG. |
| Bmp | `102` | Esegue il rendering di una pagina del documento e la salva come file BMP. |
| Emf | `103` | Esegue il rendering di una pagina del documento e la salva come file EMF (Enhanced Meta File) vettoriale. |
| Jpeg | `104` | Esegue il rendering di una pagina del documento e la salva come file JPEG. |
| Gif | `105` | Esegue il rendering di una pagina del documento e la salva come file GIF. |
| Eps | `106` | Esegue il rendering di una pagina del documento e la salva come file EPS. |
| WebP | `107` | Esegue il rendering di una pagina del documento e la salva come file WebP. |

## Esempi

Mostra come convertire dal formato DOCX al formato HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToHtml.html", SaveFormat.Html);
```

### Guarda anche

* method [Save](../document/save/)
* class [SaveOptions](../../aspose.words.saving/saveoptions/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
