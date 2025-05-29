---
title: MailMergeOptions.UseNonMergeFields
linktitle: UseNonMergeFields
articleTitle: UseNonMergeFields
second_title: Aspose.Words per .NET
description: Sblocca funzionalità avanzate di stampa unione con la proprietà UseNonMergeFields. Integra perfettamente MERGEFIELD e altri tipi di campo per una migliore personalizzazione dei documenti.
type: docs
weight: 130
url: /it/net/aspose.words.lowcode/mailmergeoptions/usenonmergefields/
---
## MailMergeOptions.UseNonMergeFields property

Quando`VERO` , specifica che oltre ai campi MERGEFIELD, la stampa unione viene eseguita in alcuni altri tipi di campi e anche nei tag "{{fieldName}}".

```csharp
public bool UseNonMergeFields { get; set; }
```

## Osservazioni

Normalmente, la stampa unione viene eseguita solo nei campi MERGEFIELD, ma diversi clienti avevano creato i propri reporting utilizzando altri campi e molti documenti in questo modo. Per semplificare la migrazione (e poiché questo approccio era utilizzato in modo indipendente da diversi clienti), è stata introdotta la possibilità di eseguire la stampa unione in altri campi.

Quando`UseNonMergeFields` è impostato su`VERO`Aspose.Words eseguirà la stampa unione nei seguenti campi:

MERGEFIELD Nome campo

MACROBUTTON NOMACRO FieldName

SE 0 = 0 "{NomeCampo}" ""

Inoltre, quando`UseNonMergeFields` è impostato su`VERO`Aspose.Words eseguirà la stampa unione nei tag di testo "{{fieldName}}". Questi non sono campi, ma solo tag di testo.

### Guarda anche

* class [MailMergeOptions](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
