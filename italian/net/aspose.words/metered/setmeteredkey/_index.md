---
title: Metered.SetMeteredKey
second_title: Aspose.Words per .NET API Reference
description: Metered metodo. Imposta la chiave pubblica e privata misurata. Se acquisti una licenza misurata quando avvii lapplicazione questa API dovrebbe essere chiamata normalmente questo è sufficiente. Tuttavia se non si riesce sempre a caricare i dati sul consumo e si superano le 24 ore la licenza verrà impostata sullo stato di valutazione per evitare tale caso è necessario controllare regolarmente lo stato della licenza se è lo stato di valutazione richiamare nuovamente questa API.
type: docs
weight: 20
url: /it/net/aspose.words/metered/setmeteredkey/
---
## Metered.SetMeteredKey method

Imposta la chiave pubblica e privata misurata. Se acquisti una licenza misurata, quando avvii l'applicazione, questa API dovrebbe essere chiamata, normalmente, questo è sufficiente. Tuttavia, se non si riesce sempre a caricare i dati sul consumo e si superano le 24 ore, la licenza verrà impostata sullo stato di valutazione, per evitare tale caso, è necessario controllare regolarmente lo stato della licenza, se è lo stato di valutazione, richiamare nuovamente questa API.

```csharp
public void SetMeteredKey(string publicKey, string privateKey)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| publicKey | String | chiave pubblica |
| privateKey | String | chiave privata |

### Esempi

Mostra come attivare una licenza a consumo e tenere traccia del credito/consumo.

```csharp
// Crea una nuova licenza a consumo, quindi stampa le relative statistiche di utilizzo.
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// Opera utilizzando Aspose.Words, quindi stampa nuovamente le nostre statistiche misurate per vedere quanto abbiamo speso.
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// Il meccanismo di licenza Aspose Metered non invia ogni volta i dati di utilizzo al server acquistato,
// devi usare wait.
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### Guarda anche

* class [Metered](../)
* spazio dei nomi [Aspose.Words](../../metered/)
* assemblea [Aspose.Words](../../../)


