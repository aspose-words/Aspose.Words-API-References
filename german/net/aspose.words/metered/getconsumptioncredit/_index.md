---
title: Metered.GetConsumptionCredit
linktitle: GetConsumptionCredit
articleTitle: GetConsumptionCredit
second_title: Aspose.Words für .NET
description: Sparen Sie Geld mit der Metered GetConsumptionCredit-Methode – rufen Sie Ihre Verbrauchsgutschriften effizient ab und sorgen Sie so für ein intelligenteres Energiemanagement.
type: docs
weight: 40
url: /de/net/aspose.words/metered/getconsumptioncredit/
---
## Metered.GetConsumptionCredit method

Erhält Verbrauchsguthaben

```csharp
public static decimal GetConsumptionCredit()
```

### Rückgabewert

Verbrauchsmenge

## Beispiele

Zeigt, wie Sie eine getaktete Lizenz aktivieren und Guthaben/Verbrauch verfolgen.

```csharp
// Erstellen Sie eine neue getaktete Lizenz und drucken Sie dann ihre Nutzungsstatistiken aus.
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Is metered license accepted: {Metered.IsMeteredLicensed()}");
Console.WriteLine($"Product name: {metered.GetProductName()}");
Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// Arbeiten Sie mit Aspose.Words und drucken Sie dann unsere Messstatistiken erneut aus, um zu sehen, wie viel wir ausgegeben haben.
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// Der Aspose Metered Licensing-Mechanismus sendet die Nutzungsdaten nicht jedes Mal an den Kaufserver.
// Sie müssen warten.
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### Siehe auch

* class [Metered](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
