---
title: "Metered"
linktitle: "Metered"
second_title: "Aspose.Words für Java"
description: "Stellt Methoden zum Festlegen des Metered-Schlüssels in Java bereit."
type: docs
weight: 469
url: /de/java/com.aspose.words/metered/
---

**Inheritance:**
java.lang.Object
```
public class Metered
```

Stellt Methoden zum Festlegen des gemessenen Schlüssels bereit.

 **Examples:** 

Zeigt, wie man eine Metered-Lizenz aktiviert und Kredit/Verbrauch verfolgt.

```

 // Create a new Metered license, and then print its usage statistics.
 Metered metered = new Metered();
 metered.setMeteredKey("MyPublicKey", "MyPrivateKey");

 System.out.println("Is metered license accepted: {Metered.IsMeteredLicensed()}");
 System.out.println("Product name: {metered.GetProductName()}");
 System.out.println("Credit before operation: {Metered.GetConsumptionCredit()}");
 System.out.println("Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

 // Operate using Aspose.Words, and then print our metered stats again to see how much we spent.
 Document doc = new Document(getMyDir() + "Document.docx");
 doc.save(getArtifactsDir() + "Metered.Usage.pdf");

 // Aspose Metered Licensing mechanism does not send the usage data to purchase server every time,
 // you need to use waiting.
 Thread.sleep(10000);

 System.out.println(MessageFormat.format("Credit after operation: {0}", Metered.getConsumptionCredit()));
 System.out.println(MessageFormat.format("Consumption quantity after operation: {0}", Metered.getConsumptionQuantity()));
 
```
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [Metered()](#Metered) | Initialisiert eine neue Instanz dieser Klasse. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getConsumptionCredit()](#getConsumptionCredit) | Ruft das Verbrauchsguthaben ab. |
| [getConsumptionQuantity()](#getConsumptionQuantity) | Ruft die Verbrauchsdateigröße ab. |
| [getProductName()](#getProductName) | Gibt den Produktnamen zurück. |
| [isMeteredLicensed()](#isMeteredLicensed) | Überprüfen, ob Metered lizenziert ist |
| [setMeteredKey(String publicKey, String privateKey)](#setMeteredKey-java.lang.String-java.lang.String) | Setzt den öffentlichen und privaten Schlüssel für Metered. |
### Metered() {#Metered}
```
public Metered()
```


Initialisiert eine neue Instanz dieser Klasse.

 **Examples:** 

Zeigt, wie man eine Metered-Lizenz aktiviert und Kredit/Verbrauch verfolgt.

```

 // Create a new Metered license, and then print its usage statistics.
 Metered metered = new Metered();
 metered.setMeteredKey("MyPublicKey", "MyPrivateKey");

 System.out.println("Is metered license accepted: {Metered.IsMeteredLicensed()}");
 System.out.println("Product name: {metered.GetProductName()}");
 System.out.println("Credit before operation: {Metered.GetConsumptionCredit()}");
 System.out.println("Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

 // Operate using Aspose.Words, and then print our metered stats again to see how much we spent.
 Document doc = new Document(getMyDir() + "Document.docx");
 doc.save(getArtifactsDir() + "Metered.Usage.pdf");

 // Aspose Metered Licensing mechanism does not send the usage data to purchase server every time,
 // you need to use waiting.
 Thread.sleep(10000);

 System.out.println(MessageFormat.format("Credit after operation: {0}", Metered.getConsumptionCredit()));
 System.out.println(MessageFormat.format("Consumption quantity after operation: {0}", Metered.getConsumptionQuantity()));
 
```

### getConsumptionCredit() {#getConsumptionCredit}
```
public static BigDecimal getConsumptionCredit()
```


Ruft das Verbrauchsguthaben ab.

 **Examples:** 

Zeigt, wie man eine Metered-Lizenz aktiviert und Kredit/Verbrauch verfolgt.

```

 // Create a new Metered license, and then print its usage statistics.
 Metered metered = new Metered();
 metered.setMeteredKey("MyPublicKey", "MyPrivateKey");

 System.out.println("Is metered license accepted: {Metered.IsMeteredLicensed()}");
 System.out.println("Product name: {metered.GetProductName()}");
 System.out.println("Credit before operation: {Metered.GetConsumptionCredit()}");
 System.out.println("Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

 // Operate using Aspose.Words, and then print our metered stats again to see how much we spent.
 Document doc = new Document(getMyDir() + "Document.docx");
 doc.save(getArtifactsDir() + "Metered.Usage.pdf");

 // Aspose Metered Licensing mechanism does not send the usage data to purchase server every time,
 // you need to use waiting.
 Thread.sleep(10000);

 System.out.println(MessageFormat.format("Credit after operation: {0}", Metered.getConsumptionCredit()));
 System.out.println(MessageFormat.format("Consumption quantity after operation: {0}", Metered.getConsumptionQuantity()));
 
```

**Returns:**
java.math.BigDecimal - Verbrauchsmenge
### getConsumptionQuantity() {#getConsumptionQuantity}
```
public static BigDecimal getConsumptionQuantity()
```


Ruft die Verbrauchsdateigröße ab.

 **Examples:** 

Zeigt, wie man eine Metered-Lizenz aktiviert und Kredit/Verbrauch verfolgt.

```

 // Create a new Metered license, and then print its usage statistics.
 Metered metered = new Metered();
 metered.setMeteredKey("MyPublicKey", "MyPrivateKey");

 System.out.println("Is metered license accepted: {Metered.IsMeteredLicensed()}");
 System.out.println("Product name: {metered.GetProductName()}");
 System.out.println("Credit before operation: {Metered.GetConsumptionCredit()}");
 System.out.println("Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

 // Operate using Aspose.Words, and then print our metered stats again to see how much we spent.
 Document doc = new Document(getMyDir() + "Document.docx");
 doc.save(getArtifactsDir() + "Metered.Usage.pdf");

 // Aspose Metered Licensing mechanism does not send the usage data to purchase server every time,
 // you need to use waiting.
 Thread.sleep(10000);

 System.out.println(MessageFormat.format("Credit after operation: {0}", Metered.getConsumptionCredit()));
 System.out.println(MessageFormat.format("Consumption quantity after operation: {0}", Metered.getConsumptionQuantity()));
 
```

**Returns:**
java.math.BigDecimal - Verbrauchsmenge
### getProductName() {#getProductName}
```
public String getProductName()
```


Gibt den Produktnamen zurück.

 **Examples:** 

Zeigt, wie man eine Metered-Lizenz aktiviert und Kredit/Verbrauch verfolgt.

```

 // Create a new Metered license, and then print its usage statistics.
 Metered metered = new Metered();
 metered.setMeteredKey("MyPublicKey", "MyPrivateKey");

 System.out.println("Is metered license accepted: {Metered.IsMeteredLicensed()}");
 System.out.println("Product name: {metered.GetProductName()}");
 System.out.println("Credit before operation: {Metered.GetConsumptionCredit()}");
 System.out.println("Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

 // Operate using Aspose.Words, and then print our metered stats again to see how much we spent.
 Document doc = new Document(getMyDir() + "Document.docx");
 doc.save(getArtifactsDir() + "Metered.Usage.pdf");

 // Aspose Metered Licensing mechanism does not send the usage data to purchase server every time,
 // you need to use waiting.
 Thread.sleep(10000);

 System.out.println(MessageFormat.format("Credit after operation: {0}", Metered.getConsumptionCredit()));
 System.out.println(MessageFormat.format("Consumption quantity after operation: {0}", Metered.getConsumptionQuantity()));
 
```

**Returns:**
java.lang.String - Produktname
### isMeteredLicensed() {#isMeteredLicensed}
```
public static boolean isMeteredLicensed()
```


Überprüfen, ob Metered lizenziert ist

 **Examples:** 

Zeigt, wie man eine Metered-Lizenz aktiviert und Kredit/Verbrauch verfolgt.

```

 // Create a new Metered license, and then print its usage statistics.
 Metered metered = new Metered();
 metered.setMeteredKey("MyPublicKey", "MyPrivateKey");

 System.out.println("Is metered license accepted: {Metered.IsMeteredLicensed()}");
 System.out.println("Product name: {metered.GetProductName()}");
 System.out.println("Credit before operation: {Metered.GetConsumptionCredit()}");
 System.out.println("Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

 // Operate using Aspose.Words, and then print our metered stats again to see how much we spent.
 Document doc = new Document(getMyDir() + "Document.docx");
 doc.save(getArtifactsDir() + "Metered.Usage.pdf");

 // Aspose Metered Licensing mechanism does not send the usage data to purchase server every time,
 // you need to use waiting.
 Thread.sleep(10000);

 System.out.println(MessageFormat.format("Credit after operation: {0}", Metered.getConsumptionCredit()));
 System.out.println(MessageFormat.format("Consumption quantity after operation: {0}", Metered.getConsumptionQuantity()));
 
```

**Returns:**
boolean - Wahr oder falsch
### setMeteredKey(String publicKey, String privateKey) {#setMeteredKey-java.lang.String-java.lang.String}
```
public void setMeteredKey(String publicKey, String privateKey)
```


Setzt den öffentlichen und privaten Schlüssel für Metered. Wenn Sie eine Metered-Lizenz erwerben, sollte diese API beim Start der Anwendung aufgerufen werden; normalerweise reicht das aus. Wenn jedoch immer wieder das Hochladen von Verbrauchsdaten fehlschlägt und 24 Stunden überschritten werden, wird die Lizenz auf den Evaluierungsstatus gesetzt. Um einen solchen Fall zu vermeiden, sollten Sie den Lizenzstatus regelmäßig prüfen; ist er im Evaluierungsstatus, rufen Sie diese API erneut auf.

 **Examples:** 

Zeigt, wie man eine Metered-Lizenz aktiviert und Kredit/Verbrauch verfolgt.

```

 // Create a new Metered license, and then print its usage statistics.
 Metered metered = new Metered();
 metered.setMeteredKey("MyPublicKey", "MyPrivateKey");

 System.out.println("Is metered license accepted: {Metered.IsMeteredLicensed()}");
 System.out.println("Product name: {metered.GetProductName()}");
 System.out.println("Credit before operation: {Metered.GetConsumptionCredit()}");
 System.out.println("Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

 // Operate using Aspose.Words, and then print our metered stats again to see how much we spent.
 Document doc = new Document(getMyDir() + "Document.docx");
 doc.save(getArtifactsDir() + "Metered.Usage.pdf");

 // Aspose Metered Licensing mechanism does not send the usage data to purchase server every time,
 // you need to use waiting.
 Thread.sleep(10000);

 System.out.println(MessageFormat.format("Credit after operation: {0}", Metered.getConsumptionCredit()));
 System.out.println(MessageFormat.format("Consumption quantity after operation: {0}", Metered.getConsumptionQuantity()));
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| publicKey | java.lang.String | öffentlicher Schlüssel |
| privateKey | java.lang.String | privater Schlüssel |

