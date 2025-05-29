---
title: WarningSource Enum
linktitle: WarningSource
articleTitle: WarningSource
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.WarningSource, che identifica le fonti di avviso durante il caricamento e il salvataggio dei documenti per una migliore gestione dei documenti.
type: docs
weight: 7500
url: /it/net/aspose.words/warningsource/
---
## WarningSource enumeration

Specifica il modulo che produce un avviso durante il caricamento o il salvataggio del documento.

```csharp
public enum WarningSource
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Unknown | `0` | La fonte dell'avviso non è specificata. |
| Layout | `1` | Modulo che crea il layout di un documento. |
| DrawingML | `2` | Modulo che esegue il rendering delle forme DrawingML. |
| OfficeMath | `3` | Modulo che esegue il rendering di OfficeMath. |
| Shapes | `4` | Modulo che esegue il rendering di forme ordinarie. |
| Metafile | `5` | Modulo che esegue il rendering dei metafile. |
| Xps | `6` | Modulo che esegue il rendering di XPS. |
| Pdf | `7` | Modulo che esegue il rendering di PDF. |
| Image | `8` | Modulo che esegue il rendering delle immagini. |
| Docx | `9` | Modulo che legge/scrive file DOCX. |
| Doc | `10` | Modulo che legge/scrive file DOC binari. |
| Text | `11` | Modulo che legge/scrive file di testo normale. |
| Rtf | `12` | Modulo che legge/scrive file RTF. |
| WordML | `13` | Modulo che legge/scrive file WML. |
| Nrx | `14` | Moduli comuni condivisi tra i moduli di lettura/scrittura DOCX/WML. |
| Odt | `15` | Modulo che legge/scrive file ODT. |
| Html | `16` | Modulo che legge/scrive file HTML/MHTML. |
| Validator | `17` | Modulo che verifica la coerenza e la validità del modello. |
| Xaml | `18` | Modulo che legge/scrive file Xaml. |
| Svm | `19` | Modulo che legge i file Svm. |
| MathML | `20` | Modulo che legge i file W3C MathML. |
| Font | `21` | Modulo che legge i file dei font. |
| Svg | `22` | Modulo che legge i file SVG. |
| Markdown | `23` | Modulo che legge/scrive file Markdown. |
| Chm | `24` | Modulo che legge i file CHM. |
| Epub | `25` | Modulo che legge/scrive file EPUB. |
| Xml | `26` | Modulo che legge i file XML. |
| Xlsx | `27` | Modulo che scrive i file XLSX. |

## Esempi

Mostra come lavorare con la sorgente di avviso.

```csharp
Document doc = new Document(MyDir + "Emphases markdown warning.docx");

WarningInfoCollection warnings = new WarningInfoCollection();
doc.WarningCallback = warnings;
doc.Save(ArtifactsDir + "DocumentBuilder.EmphasesWarningSourceMarkdown.md");

foreach (WarningInfo warningInfo in warnings)
{
    if (warningInfo.Source == WarningSource.Markdown)
        Assert.AreEqual("The (*, 0:11) cannot be properly written into Markdown.", warningInfo.Description);
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
