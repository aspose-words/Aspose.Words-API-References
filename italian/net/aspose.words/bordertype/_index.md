---
title: Enum BorderType
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.BorderType enum. Specifica i lati di un bordo.
type: docs
weight: 90
url: /it/net/aspose.words/bordertype/
---
## BorderType enumeration

Specifica i lati di un bordo.

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
| Horizontal | `4` | Specifica il bordo orizzontale tra le celle di una tabella o tra paragrafi conformi. |
| Vertical | `5` | Specifica il bordo verticale tra le celle di una tabella. |
| DiagonalDown | `6` | Specifica il bordo diagonale in una cella di tabella. |
| DiagonalUp | `7` | Specifica il bordo diagonale in una cella di tabella. |

### Esempi

Mostra come inserire un paragrafo con un bordo superiore.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders[BorderType.Top];
topBorder.Color = Color.Red;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;

builder.Writeln("Text with a red top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


