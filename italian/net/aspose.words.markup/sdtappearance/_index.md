---
title: SdtAppearance Enum
linktitle: SdtAppearance
articleTitle: SdtAppearance
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Markup.SdtAppearance per personalizzare l'aspetto dei tag dei documenti strutturati. Migliora la formattazione dei tuoi documenti senza sforzo!
type: docs
weight: 4680
url: /it/net/aspose.words.markup/sdtappearance/
---
## SdtAppearance enumeration

Specifica l'aspetto di un tag di documento strutturato.

```csharp
public enum SdtAppearance
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| BoundingBox | `0` | Rappresenta un tag di documento strutturato visualizzato come un rettangolo ombreggiato o un riquadro di delimitazione. |
| Tags | `1` | Rappresenta un tag di documento strutturato mostrato come marcatori di inizio e fine. |
| Hidden | `2` | Rappresenta un tag di documento strutturato che non viene mostrato. |
| Default | `0` | Per impostazione predefinitaBoundingBox . |

## Esempi

Mostra come visualizzare i tag attorno al contenuto.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true) as StructuredDocumentTagRangeStart;

if (tag.Appearance == SdtAppearance.Hidden)
    tag.Appearance = SdtAppearance.Tags;
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Markup](../../aspose.words.markup/)
* assemblea [Aspose.Words](../../)
