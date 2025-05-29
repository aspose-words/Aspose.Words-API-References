---
title: FieldOptions.IsBidiTextSupportedOnUpdate
linktitle: IsBidiTextSupportedOnUpdate
articleTitle: IsBidiTextSupportedOnUpdate
second_title: Aspose.Words per .NET
description: Scopri se il supporto del testo bidirezionale è abilitato in FieldOptions. Gestisci facilmente gli aggiornamenti del testo per funzionalità multilingue avanzate.
type: docs
weight: 150
url: /it/net/aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/
---
## FieldOptions.IsBidiTextSupportedOnUpdate property

Ottiene o imposta il valore che indica se il testo bidirezionale è completamente supportato durante l'aggiornamento del campo o meno.

```csharp
public bool IsBidiTextSupportedOnUpdate { get; set; }
```

## Osservazioni

Quando questa proprietà è impostata su`VERO`, vengono eseguiti ulteriori passaggi per produrre un risultato di campo compatibile con la lingua da destra a sinistra (ad esempio arabo o ebraico) durante l'aggiornamento.

Quando questa proprietà è impostata su`falso` e viene utilizzato il linguaggio da destra a sinistra, la correttezza del campo result dopo il suo aggiornamento non è garantita.

Il valore predefinito è`falso`.

## Esempi

Mostra come utilizzare FieldOptions per garantire che l'aggiornamento dei campi supporti completamente il testo bidirezionale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Assicurarsi che tutte le operazioni sui campi che coinvolgono testo da destra a sinistra vengano eseguite come previsto.
doc.FieldOptions.IsBidiTextSupportedOnUpdate = true;

// Utilizzare un generatore di documenti per inserire un campo contenente testo da destra a sinistra.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "עֶשְׂרִים", "שְׁלוֹשִׁים", "אַרְבָּעִים", "חֲמִשִּׁים", "שִׁשִּׁים" }, 0);
comboBox.CalculateOnExit = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.Bidi.docx");
```

### Guarda anche

* class [FieldOptions](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
