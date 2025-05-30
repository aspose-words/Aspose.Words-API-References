---
title: StructuredDocumentTag.Checked
linktitle: Checked
articleTitle: Checked
second_title: Aspose.Words per .NET
description: Gestisci la casella di controllo SDT con la proprietà Checked di StructuredDocumentTag. Ottieni/imposta facilmente il suo stato il valore predefinito è "false". Migliora l'interattività dei documenti oggi stesso!
type: docs
weight: 60
url: /it/net/aspose.words.markup/structureddocumenttag/checked/
---
## StructuredDocumentTag.Checked property

Ottiene/imposta lo stato corrente della casella di controllo**SDT** . Il valore predefinito per questa proprietà è`falso` .

```csharp
public bool Checked { get; set; }
```

## Osservazioni

L'accesso a questa proprietà funzionerà solo perCheckbox tipi SDT.

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
