---
title: StructuredDocumentTag.SetCheckedSymbol
linktitle: SetCheckedSymbol
articleTitle: SetCheckedSymbol
second_title: Aspose.Words per .NET
description: Scopri come utilizzare il metodo SetCheckedSymbol in StructuredDocumentTag per personalizzare gli elementi visivi delle caselle di controllo e migliorare l'esperienza utente.
type: docs
weight: 380
url: /it/net/aspose.words.markup/structureddocumenttag/setcheckedsymbol/
---
## StructuredDocumentTag.SetCheckedSymbol method

Imposta il simbolo utilizzato per rappresentare lo stato selezionato di un controllo del contenuto della casella di controllo.

```csharp
public void SetCheckedSymbol(int characterCode, string fontName)
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
