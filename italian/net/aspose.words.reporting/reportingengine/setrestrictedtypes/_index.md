---
title: ReportingEngine.SetRestrictedTypes
linktitle: SetRestrictedTypes
articleTitle: SetRestrictedTypes
second_title: Aspose.Words per .NET
description: Scopri come il metodo SetRestrictedTypes in ReportingEngine migliora la sicurezza limitando l'accesso dei membri nella sintassi del modello per un reporting dei dati ottimizzato.
type: docs
weight: 80
url: /it/net/aspose.words.reporting/reportingengine/setrestrictedtypes/
---
## ReportingEngine.SetRestrictedTypes method

Specifica i tipi, quali membri e quali membri dei tipi derivati non devono essere accessibili al motore tramite la sintassi del modello.

```csharp
public static void SetRestrictedTypes(params Type[] types)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| types | Type[] | Tipi da limitare. |

## Osservazioni

I tipi limitati dovrebbero essere impostati prima della prima creazione di un report. Dopo`Report di costruzione` viene invocato, i tipi con restrizioni non possono essere modificati e viene generata un'eccezione nel tentativo di farlo. Il posto migliore per impostare i tipi con restrizioni è l'avvio dell'applicazione.

Si noti che una grande quantità di tipi limitati può influire sulle prestazioni, quindi è meglio limitare solo quei tipi il cui accesso ai membri è davvero sensibile.

LanciArgumentException nei seguenti casi:

-*types* è nullo.

- Uno di*types* gli articoli sono`null`.

- Uno di*types* items rappresenta un tipo invisibile, vale a dire un tipo non pubblico oppure un tipo pubblico annidato che ha un tipo esterno non pubblico.

- Uno di*types* items rappresenta un tipo array.

-*types* contengono voci duplicate.

## Esempi

Mostra come negare l'accesso ai membri di tipi considerati non sicuri.

```csharp
Document doc =
    DocumentHelper.CreateSimpleDocument(
        "<<var [typeVar = \"\".GetType().BaseType]>><<[typeVar]>>");

// Tieni presente che non è possibile impostare tipi con restrizioni durante o dopo la creazione di un report.
ReportingEngine.SetRestrictedTypes(typeof(System.Type));
// Impostiamo l'opzione "AllowMissingMembers" per evitare eccezioni durante la creazione di un report.
ReportingEngine engine = new ReportingEngine() { Options = ReportBuildOptions.AllowMissingMembers };
engine.BuildReport(doc, new object());

// Otteniamo una stringa vuota perché non possiamo accedere al metodo GetType().
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### Guarda anche

* class [ReportingEngine](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)
