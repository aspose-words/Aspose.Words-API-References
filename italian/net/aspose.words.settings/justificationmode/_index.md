---
title: Enum JustificationMode
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Settings.JustificationMode enum. Specifica la regolazione della spaziatura dei caratteri per un documento. Il valore predefinito èEspandere .
type: docs
weight: 5800
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
| Expand | `0` |  |
| Compress | `1` |  |
| CompressKana | `2` |  |

### Esempi

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


