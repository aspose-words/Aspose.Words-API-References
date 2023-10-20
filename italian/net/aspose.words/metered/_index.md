---
title: Metered Class
linktitle: Metered
articleTitle: Metered
second_title: Aspose.Words per .NET
description: Aspose.Words.Metered classe. Fornisce metodi per impostare la chiave a consumo in C#.
type: docs
weight: 4160
url: /it/net/aspose.words/metered/
---
## Metered class

Fornisce metodi per impostare la chiave a consumo.

Per saperne di più, visita il[Licenza e abbonamento](https://docs.aspose.com/words/net/licensing/) articolo di documentazione.

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
| [SetMeteredKey](../../aspose.words/metered/setmeteredkey/)(*string, string*) | Imposta la chiave pubblica e privata misurata. Se acquisti una licenza misurata, quando avvii l'applicazione, questa API dovrebbe essere chiamata, normalmente, questo è sufficiente. Tuttavia, se non si riesce sempre a caricare i dati sul consumo e si superano le 24 ore, la licenza verrà impostata sullo stato di valutazione, per evitare tale caso, è necessario controllare regolarmente lo stato della licenza, se è lo stato di valutazione, richiamare nuovamente questa API. |
| static [GetConsumptionCredit](../../aspose.words/metered/getconsumptioncredit/)() | Ottiene credito di consumo |
| static [GetConsumptionQuantity](../../aspose.words/metered/getconsumptionquantity/)() | Ottiene la dimensione del file di consumo |

## Esempi

In questo esempio, verrà effettuato un tentativo di impostare la chiave pubblica e privata a consumo

```csharp
[C#]

Metered matered = new Metered();
matered.SetMeteredKey("PublicKey", "PrivateKey");


[Visual Basic]

Dim matered As Metered = New Metered
matered.SetMeteredKey("PublicKey", "PrivateKey")
```

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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
