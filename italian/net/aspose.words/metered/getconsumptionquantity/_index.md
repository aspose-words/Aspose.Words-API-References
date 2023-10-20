---
title: Metered.GetConsumptionQuantity
linktitle: GetConsumptionQuantity
articleTitle: GetConsumptionQuantity
second_title: Aspose.Words per .NET
description: Metered GetConsumptionQuantity metodo. Ottiene la dimensione del file di consumo in C#.
type: docs
weight: 40
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
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
