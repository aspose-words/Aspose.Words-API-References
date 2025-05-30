---
title: Metered.GetConsumptionCredit
linktitle: GetConsumptionCredit
articleTitle: GetConsumptionCredit
second_title: Aspose.Words per .NET
description: Sblocca i risparmi con il metodo Metered GetConsumptionCredit recupera in modo efficiente i tuoi crediti di consumo per una gestione più intelligente dell'energia.
type: docs
weight: 40
url: /it/net/aspose.words/metered/getconsumptioncredit/
---
## Metered.GetConsumptionCredit method

Ottiene credito di consumo

```csharp
public static decimal GetConsumptionCredit()
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
