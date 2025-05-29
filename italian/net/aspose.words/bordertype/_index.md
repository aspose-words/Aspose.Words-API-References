---
title: BorderType Enum
linktitle: BorderType
articleTitle: BorderType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.BorderType per opzioni di bordo personalizzabili. Migliora i tuoi documenti con un controllo preciso dei bordi e uno stile impeccabile!
type: docs
weight: 290
url: /it/net/aspose.words/bordertype/
---
## BorderType enumeration

Specifica i lati di un bordo.

Per saperne di più, visita il[Programmazione con documenti](https://docs.aspose.com/words/net/programming-with-documents/) articolo di documentazione.

```csharp
public enum BorderType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `-1` | Valore predefinito. |
| Bottom | `0` | Specifica il bordo inferiore di un paragrafo o di una cella di tabella. |
| Left | `1` | Specifica il bordo sinistro di un paragrafo o di una cella di tabella. |
| Right | `2` | Specifica il bordo destro di un paragrafo o di una cella di tabella. |
| Top | `3` | Specifica il bordo superiore di un paragrafo o di una cella di tabella. |
| Horizontal | `4` | Specifica il bordo orizzontale tra le celle in una tabella o tra paragrafi conformi. |
| Vertical | `5` | Specifica il bordo verticale tra le celle in una tabella. |
| DiagonalDown | `6` | Specifica il bordo diagonale in una cella di tabella. |
| DiagonalUp | `7` | Specifica il bordo diagonale in una cella di tabella. |

## Esempi

Mostra come inserire un paragrafo con un bordo superiore.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// Imposta ThemeColor solo quando è impostato LineWidth o LineStyle.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
