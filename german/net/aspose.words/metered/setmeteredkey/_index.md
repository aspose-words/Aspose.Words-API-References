---
title: Metered.SetMeteredKey
linktitle: SetMeteredKey
articleTitle: SetMeteredKey
second_title: Aspose.Words für .NET
description: Verwalten Sie Ihre gemessene Lizenz mühelos mit der SetMeteredKey-Methode. Sorgen Sie für reibungslose Datenuploads und vermeiden Sie Evaluierungsstatus durch regelmäßige Überprüfungen.
type: docs
weight: 30
url: /de/net/aspose.words/metered/setmeteredkey/
---
## Metered.SetMeteredKey method

Legt den öffentlichen und privaten Schlüssel mit Nutzungsdauer fest. Wenn Sie eine Lizenz mit Nutzungsdauer erwerben, sollte diese API beim Starten der Anwendung aufgerufen werden. Normalerweise reicht dies aus. Wenn das Hochladen der Verbrauchsdaten jedoch immer fehlschlägt und 24 Stunden überschritten werden, wird die Lizenz auf den Evaluierungsstatus gesetzt. Um dies zu vermeiden, sollten Sie den Lizenzstatus regelmäßig überprüfen. Wenn es sich um den Evaluierungsstatus handelt, rufen Sie diese API erneut auf.

```csharp
public void SetMeteredKey(string publicKey, string privateKey)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| publicKey | String | öffentlicher Schlüssel |
| privateKey | String | privater Schlüssel |

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
