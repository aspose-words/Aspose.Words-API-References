---
title: JustificationMode Enum
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words JustificationMode per regolazioni precise della spaziatura dei caratteri nei tuoi documenti. Migliora la leggibilità con impostazioni personalizzabili!
type: docs
weight: 6630
url: /it/net/aspose.words.settings/justificationmode/
---
## JustificationMode enumeration

Specifica la regolazione della spaziatura dei caratteri per un documento. Il valore predefinito è`Espandere` .

```csharp
public enum JustificationMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Expand | `0` | Non comprimere la spaziatura dei caratteri. |
| Compress | `1` | Comprimi la spaziatura dei caratteri. |
| CompressKana | `2` | Comprimi, usando le regole dei sillabari kana, Hiragana e Katakana. |

## Esempi

Mostra come gestire il controllo della spaziatura dei caratteri.

```csharp
Document doc = new Document(MyDir + "Document.docx");

JustificationMode justificationMode = doc.JustificationMode;
if (justificationMode == JustificationMode.Expand)
    doc.JustificationMode = JustificationMode.Compress;

doc.Save(ArtifactsDir + "Document.SetJustificationMode.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Settings](../../aspose.words.settings/)
* assemblea [Aspose.Words](../../)
