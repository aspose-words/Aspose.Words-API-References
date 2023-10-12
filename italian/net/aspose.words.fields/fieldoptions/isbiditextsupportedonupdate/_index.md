---
title: FieldOptions.IsBidiTextSupportedOnUpdate
second_title: Aspose.Words per .NET API Reference
description: FieldOptions proprietà. Ottiene o imposta il valore che indica se il testo bidirezionale è completamente supportato durante laggiornamento del campo o meno.
type: docs
weight: 150
url: /it/net/aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/
---
## FieldOptions.IsBidiTextSupportedOnUpdate property

Ottiene o imposta il valore che indica se il testo bidirezionale è completamente supportato durante l'aggiornamento del campo o meno.

```csharp
public bool IsBidiTextSupportedOnUpdate { get; set; }
```

### Osservazioni

Quando questa proprietà è impostata su`VERO`, vengono eseguiti passaggi aggiuntivi per produrre risultati di campi compatibili con la lingua da destra a sinistra (ad esempio arabo o ebraico) durante l'aggiornamento.

Quando questa proprietà è impostata su`falso` e viene utilizzata la lingua da destra a sinistra, la correttezza del campo result dopo il suo aggiornamento non è garantita.

Il valore predefinito è`falso`.

### Esempi

Mostra come utilizzare FieldOptions per garantire che l'aggiornamento dei campi supporti completamente il testo bidirezionale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Assicurarsi che qualsiasi operazione sul campo che coinvolga il testo da destra a sinistra venga eseguita come previsto.
doc.FieldOptions.IsBidiTextSupportedOnUpdate = true;

// Utilizzare un generatore di documenti per inserire un campo che contenga il testo da destra a sinistra.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "עֶשְׂרִים", "שְׁלוֹשִׁים", "אַרְבָּעִים", "חֲמִשִּׁים", "שִׁשִּׁים" }, 0);
comboBox.CalculateOnExit = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.Bidi.docx");
```

### Guarda anche

* class [FieldOptions](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldoptions/)
* assemblea [Aspose.Words](../../../)


