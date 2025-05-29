---
title: Metered Class
linktitle: Metered
articleTitle: Metered
second_title: Aspose.Words für .NET
description: Entfesseln Sie die Leistungsfähigkeit der Aspose.Words.Metered-Klasse! Verwalten Sie Ihren Messschlüssel ganz einfach mit effizienten Methoden für eine nahtlose Dokumentenverarbeitung.
type: docs
weight: 4850
url: /de/net/aspose.words/metered/
---
## Metered class

Bietet Methoden zum Festlegen des gemessenen Schlüssels.

```csharp
public class Metered
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [Metered](metered/)() | Initialisiert eine neue Instanz dieser Klasse. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetProductName](../../aspose.words/metered/getproductname/)() | Retouren Produktname |
| [SetMeteredKey](../../aspose.words/metered/setmeteredkey/)(*string, string*) | Legt den öffentlichen und privaten Schlüssel mit Nutzungsdauer fest. Wenn Sie eine Lizenz mit Nutzungsdauer erwerben, sollte diese API beim Starten der Anwendung aufgerufen werden. Normalerweise reicht dies aus. Wenn das Hochladen der Verbrauchsdaten jedoch immer fehlschlägt und 24 Stunden überschritten werden, wird die Lizenz auf den Evaluierungsstatus gesetzt. Um dies zu vermeiden, sollten Sie den Lizenzstatus regelmäßig überprüfen. Wenn es sich um den Evaluierungsstatus handelt, rufen Sie diese API erneut auf. |
| static [GetConsumptionCredit](../../aspose.words/metered/getconsumptioncredit/)() | Erhält Verbrauchsguthaben |
| static [GetConsumptionQuantity](../../aspose.words/metered/getconsumptionquantity/)() | Ruft die Verbrauchsdateigröße ab |
| static [IsMeteredLicensed](../../aspose.words/metered/ismeteredlicensed/)() | Prüfen, ob Metered lizenziert ist |

## Beispiele

In diesem Beispiel wird versucht, gemessene öffentliche und private Schlüssel festzulegen

```csharp
[C#]

Metered matered = new Metered();
matered.SetMeteredKey("PublicKey", "PrivateKey");


[Visual Basic]

Dim matered As Metered = New Metered
matered.SetMeteredKey("PublicKey", "PrivateKey")
```

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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
