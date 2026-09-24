---
title: "Metered"
linktitle: "Metered"
second_title: "Aspose.Words para Java"
description: "Proporciona métodos para establecer la clave metered en Java."
type: docs
weight: 469
url: /es/java/com.aspose.words/metered/
---

**Inheritance:**
java.lang.Object
```
public class Metered
```

Proporciona métodos para establecer la clave medida.

 **Examples:** 

Muestra cómo activar una licencia Metered y rastrear el crédito/consumo.

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
## Constructores

| Constructor | Descripción |
| --- | --- |
| [Metered()](#Metered) | Inicializa una nueva instancia de esta clase. |
## Métodos

| Método | Descripción |
| --- | --- |
| [getConsumptionCredit()](#getConsumptionCredit) | Obtiene el crédito de consumo |
| [getConsumptionQuantity()](#getConsumptionQuantity) | Obtiene el tamaño del archivo de consumo |
| [getProductName()](#getProductName) | Devuelve el nombre del producto |
| [isMeteredLicensed()](#isMeteredLicensed) | Comprueba si Metered está licenciado |
| [setMeteredKey(String publicKey, String privateKey)](#setMeteredKey-java.lang.String-java.lang.String) | Establece la clave pública y privada de Metered. |
### Metered() {#Metered}
```
public Metered()
```


Inicializa una nueva instancia de esta clase.

 **Examples:** 

Muestra cómo activar una licencia Metered y rastrear el crédito/consumo.

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


Obtiene el crédito de consumo

 **Examples:** 

Muestra cómo activar una licencia Metered y rastrear el crédito/consumo.

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
java.math.BigDecimal - cantidad de consumo
### getConsumptionQuantity() {#getConsumptionQuantity}
```
public static BigDecimal getConsumptionQuantity()
```


Obtiene el tamaño del archivo de consumo

 **Examples:** 

Muestra cómo activar una licencia Metered y rastrear el crédito/consumo.

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
java.math.BigDecimal - cantidad de consumo
### getProductName() {#getProductName}
```
public String getProductName()
```


Devuelve el nombre del producto

 **Examples:** 

Muestra cómo activar una licencia Metered y rastrear el crédito/consumo.

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
java.lang.String - Nombre del producto
### isMeteredLicensed() {#isMeteredLicensed}
```
public static boolean isMeteredLicensed()
```


Comprueba si Metered está licenciado

 **Examples:** 

Muestra cómo activar una licencia Metered y rastrear el crédito/consumo.

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
boolean - Verdadero o falso
### setMeteredKey(String publicKey, String privateKey) {#setMeteredKey-java.lang.String-java.lang.String}
```
public void setMeteredKey(String publicKey, String privateKey)
```


Establece la clave pública y privada medida. Si usted compra una licencia medida, al iniciar la aplicación, debe llamarse a esta API; normalmente, eso es suficiente. Sin embargo, si siempre falla la carga de datos de consumo y supera las 24 horas, la licencia se establecerá en estado de evaluación; para evitar tal caso, debe comprobar regularmente el estado de la licencia, y si está en estado de evaluación, llamar a esta API nuevamente.

 **Examples:** 

Muestra cómo activar una licencia Metered y rastrear el crédito/consumo.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| publicKey | java.lang.String | clave pública |
| privateKey | java.lang.String | clave privada |

