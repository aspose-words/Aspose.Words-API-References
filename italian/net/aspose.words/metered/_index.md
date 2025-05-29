---
title: Metered Class
linktitle: Metered
articleTitle: Metered
second_title: Aspose.Words per .NET
description: Sfrutta la potenza della classe Aspose.Words.Metered! Gestisci facilmente la tua chiave metered con metodi efficienti per un'elaborazione dei documenti impeccabile.
type: docs
weight: 4850
url: /it/net/aspose.words/metered/
---
## Metered class

Fornisce metodi per impostare la chiave misurata.

```csharp
public class Metered
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [Metered](metered/)() | Inizializza una nuova istanza di questa classe. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetProductName](../../aspose.words/metered/getproductname/)() | Restituisce Nome prodotto |
| [SetMeteredKey](../../aspose.words/metered/setmeteredkey/)(*string, string*) | Imposta la chiave pubblica e privata a consumo. Se acquisti una licenza a consumo, all'avvio dell'applicazione dovrebbe essere richiamata questa API; normalmente, questo è sufficiente. Tuttavia, se non si riesce a caricare i dati di consumo per più di 24 ore, la licenza verrà impostata sullo stato di valutazione. Per evitare questo caso, dovresti controllare regolarmente lo stato della licenza. Se è in stato di valutazione, richiama nuovamente questa API. |
| static [GetConsumptionCredit](../../aspose.words/metered/getconsumptioncredit/)() | Ottiene credito di consumo |
| static [GetConsumptionQuantity](../../aspose.words/metered/getconsumptionquantity/)() | Ottiene la dimensione del file di consumo |
| static [IsMeteredLicensed](../../aspose.words/metered/ismeteredlicensed/)() | Controlla se il consumo è concesso in licenza |

## Esempi

In questo esempio, verrà effettuato un tentativo di impostare la chiave pubblica e privata misurata

```csharp
[C#]

Metered matered = new Metered();
matered.SetMeteredKey("PublicKey", "PrivateKey");


[Visual Basic]

Dim matered As Metered = New Metered
matered.SetMeteredKey("PublicKey", "PrivateKey")
```

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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
