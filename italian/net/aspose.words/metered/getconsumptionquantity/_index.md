---
title: Metered.GetConsumptionQuantity
linktitle: GetConsumptionQuantity
articleTitle: GetConsumptionQuantity
second_title: Aspose.Words per .NET
description: Scopri il metodo Metered GetConsumptionQuantity per recuperare in modo efficiente i dati sulle dimensioni dei file e ottimizzare la gestione delle risorse. Migliora le tue analisi sui dati!
type: docs
weight: 50
url: /it/net/aspose.words/metered/getconsumptionquantity/
---
## Metered.GetConsumptionQuantity method

Ottiene la dimensione del file di consumo

```csharp
public static decimal GetConsumptionQuantity()
```

### Valore di ritorno

quantità di consumo

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
