---
title: Metered.SetMeteredKey
linktitle: SetMeteredKey
articleTitle: SetMeteredKey
second_title: Aspose.Words per .NET
description: Gestisci senza problemi la tua licenza a consumo con il metodo SetMeteredKey. Garantisci caricamenti dati fluidi ed evita lo stato di valutazione con controlli regolari.
type: docs
weight: 30
url: /it/net/aspose.words/metered/setmeteredkey/
---
## Metered.SetMeteredKey method

Imposta la chiave pubblica e privata a consumo. Se acquisti una licenza a consumo, all'avvio dell'applicazione dovrebbe essere richiamata questa API; normalmente, questo è sufficiente. Tuttavia, se non si riesce a caricare i dati di consumo per più di 24 ore, la licenza verrà impostata sullo stato di valutazione. Per evitare questo caso, dovresti controllare regolarmente lo stato della licenza. Se è in stato di valutazione, richiama nuovamente questa API.

```csharp
public void SetMeteredKey(string publicKey, string privateKey)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| publicKey | String | chiave pubblica |
| privateKey | String | chiave privata |

## Esempi

Mostra come attivare una licenza a consumo e monitorare credito/consumo.

```csharp
// Crea una nuova licenza a consumo e quindi stampa le statistiche di utilizzo.
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Is metered license accepted: {Metered.IsMeteredLicensed()}");
Console.WriteLine($"Product name: {metered.GetProductName()}");
Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// Operiamo utilizzando Aspose.Words, quindi stampiamo di nuovo le nostre statistiche misurate per vedere quanto abbiamo speso.
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// Il meccanismo di licenza a consumo di Aspose non invia ogni volta i dati di utilizzo al server di acquisto,
// devi usare l'attesa.
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### Guarda anche

* class [Metered](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
