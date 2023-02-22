---
title: Metered.GetConsumptionQuantity
second_title: Aspose.Words für .NET-API-Referenz
description: Metered methode. Ruft die Verbrauchsdateigröße ab
type: docs
weight: 40
url: /de/net/aspose.words/metered/getconsumptionquantity/
---
## Metered.GetConsumptionQuantity method

Ruft die Verbrauchsdateigröße ab

```csharp
public static decimal GetConsumptionQuantity()
```

### Rückgabewert

Verbrauchsmenge

### Beispiele

Zeigt, wie eine kostenpflichtige Lizenz aktiviert und Guthaben/Verbrauch nachverfolgt wird.

```csharp
// Erstellen Sie eine neue Metered-Lizenz und drucken Sie dann ihre Nutzungsstatistiken.
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// Arbeiten Sie mit Aspose.Words und drucken Sie dann unsere gemessenen Statistiken erneut aus, um zu sehen, wie viel wir ausgegeben haben.
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// Der Aspose Metered Licensing-Mechanismus sendet die Nutzungsdaten nicht jedes Mal an den Kaufserver,
// Sie müssen warten verwenden.
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### Siehe auch

* class [Metered](../)
* namensraum [Aspose.Words](../../metered/)
* Montage [Aspose.Words](../../../)


