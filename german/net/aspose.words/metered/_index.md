---
title: Class Metered
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Metered klas. Stellt Methoden zum Festlegen des gemessenen Schlüssels bereit.
type: docs
weight: 4160
url: /de/net/aspose.words/metered/
---
## Metered class

Stellt Methoden zum Festlegen des gemessenen Schlüssels bereit.

Um mehr zu erfahren, besuchen Sie die[Lizenzierung und Abonnement](https://docs.aspose.com/words/net/licensing/) Dokumentationsartikel.

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
| [SetMeteredKey](../../aspose.words/metered/setmeteredkey/)(string, string) | Legt einen gemessenen öffentlichen und privaten Schlüssel fest. Wenn Sie eine gemessene Lizenz erwerben, sollte beim Starten der Anwendung diese API aufgerufen werden. Normalerweise reicht dies aus. Wenn jedoch das Hochladen der Verbrauchsdaten immer fehlschlägt und 24 Stunden überschritten werden, wird die Lizenz auf den Evaluierungsstatus gesetzt. Um einen solchen Fall zu vermeiden, sollten Sie den Lizenzstatus regelmäßig überprüfen. Wenn es sich um den Evaluierungsstatus handelt, rufen Sie diese API erneut auf. |
| static [GetConsumptionCredit](../../aspose.words/metered/getconsumptioncredit/)() | Erhält Verbrauchsgutschrift |
| static [GetConsumptionQuantity](../../aspose.words/metered/getconsumptionquantity/)() | Ruft die Größe der Verbrauchsdatei ab |

### Beispiele

In diesem Beispiel wird versucht, einen gemessenen öffentlichen und privaten Schlüssel festzulegen

```csharp
[C#]

Metered matered = new Metered();
matered.SetMeteredKey("PublicKey", "PrivateKey");


[Visual Basic]

Dim matered As Metered = New Metered
matered.SetMeteredKey("PublicKey", "PrivateKey")
```

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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


