---
title: StructuredDocumentTag.SetUncheckedSymbol
linktitle: SetUncheckedSymbol
articleTitle: SetUncheckedSymbol
second_title: Aspose.Words per .NET
description: Scopri come il metodo SetUncheckedSymbol migliora il tuo StructuredDocumentTag personalizzando gli elementi visivi delle caselle di controllo per una migliore esperienza utente.
type: docs
weight: 390
url: /it/net/aspose.words.markup/structureddocumenttag/setuncheckedsymbol/
---
## StructuredDocumentTag.SetUncheckedSymbol method

Imposta il simbolo utilizzato per rappresentare lo stato non selezionato di un controllo del contenuto di una casella di controllo.

```csharp
public void SetUncheckedSymbol(int characterCode, string fontName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| characterCode | Int32 | Il codice carattere per il simbolo specificato. |
| fontName | String | Il nome del font che contiene il simbolo. |

## Osservazioni

L'accesso a questo metodo funzionerà solo perCheckbox Tipi di SDT.

Per tutti gli altri tipi di SDT si verificheranno delle eccezioni.

## Esempi

Mostra come creare un tag di documento strutturato sotto forma di casella di controllo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

StructuredDocumentTag sdtCheckBox =
    new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline) { Checked = true };

// Possiamo impostare i simboli utilizzati per rappresentare lo stato selezionato/deselezionato di un controllo del contenuto di una casella di controllo.
sdtCheckBox.SetCheckedSymbol(0x00A9, "Times New Roman");
sdtCheckBox.SetUncheckedSymbol(0x00AE, "Times New Roman");

builder.InsertNode(sdtCheckBox);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CheckBox.docx");
```

### Guarda anche

* class [StructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
