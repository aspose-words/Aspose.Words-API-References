---
title: Metered.SetMeteredKey
second_title: Aspose.Words für .NET-API-Referenz
description: Metered methode. Legt einen gemessenen öffentlichen und privaten Schlüssel fest. Wenn Sie eine gemessene Lizenz erwerben sollte beim Starten der Anwendung diese API aufgerufen werden. Normalerweise reicht dies aus. Wenn jedoch das Hochladen der Verbrauchsdaten immer fehlschlägt und 24 Stunden überschritten werden wird die Lizenz auf den Evaluierungsstatus gesetzt. Um einen solchen Fall zu vermeiden sollten Sie den Lizenzstatus regelmäßig überprüfen. Wenn es sich um den Evaluierungsstatus handelt rufen Sie diese API erneut auf.
type: docs
weight: 20
url: /de/net/aspose.words/metered/setmeteredkey/
---
## Metered.SetMeteredKey method

Legt einen gemessenen öffentlichen und privaten Schlüssel fest. Wenn Sie eine gemessene Lizenz erwerben, sollte beim Starten der Anwendung diese API aufgerufen werden. Normalerweise reicht dies aus. Wenn jedoch das Hochladen der Verbrauchsdaten immer fehlschlägt und 24 Stunden überschritten werden, wird die Lizenz auf den Evaluierungsstatus gesetzt. Um einen solchen Fall zu vermeiden, sollten Sie den Lizenzstatus regelmäßig überprüfen. Wenn es sich um den Evaluierungsstatus handelt, rufen Sie diese API erneut auf.

```csharp
public void SetMeteredKey(string publicKey, string privateKey)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| publicKey | String | Öffentlicher Schlüssel |
| privateKey | String | Privat Schlüssel |

### Beispiele

Zeigt, wie Sie eine Metered-Lizenz aktivieren und Guthaben/Verbrauch verfolgen.

```csharp
// Erstellen Sie eine neue Metered-Lizenz und drucken Sie dann deren Nutzungsstatistik aus.
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// Arbeiten Sie mit Aspose.Words und drucken Sie dann unsere gemessenen Statistiken erneut aus, um zu sehen, wie viel wir ausgegeben haben.
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// Der Aspose Metered Licensing-Mechanismus sendet die Nutzungsdaten nicht jedes Mal an den Kaufserver.
// Sie müssen warten verwenden.
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### Siehe auch

* class [Metered](../)
* namensraum [Aspose.Words](../../metered/)
* Montage [Aspose.Words](../../../)


