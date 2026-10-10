---
title: "Metered"
linktitle: "Metered"
second_title: "Aspose.Words для Java"
description: "Предоставляет методы для установки метерного ключа в Java."
type: docs
weight: 469
url: /ru/java/com.aspose.words/metered/
---

**Inheritance:**
java.lang.Object
```
public class Metered
```

Предоставляет методы для установки измеряемого ключа.

 **Examples:** 

Показывает, как активировать Metered‑лицензию и отслеживать кредит/потребление.

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
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [Metered()](#Metered) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [getConsumptionCredit()](#getConsumptionCredit) | Получает кредит потребления |
| [getConsumptionQuantity()](#getConsumptionQuantity) | Получает размер файла потребления |
| [getProductName()](#getProductName) | Возвращает название продукта |
| [isMeteredLicensed()](#isMeteredLicensed) | Проверяет, лицензирована ли Metered |
| [setMeteredKey(String publicKey, String privateKey)](#setMeteredKey-java.lang.String-java.lang.String) | Устанавливает публичный и приватный ключ Metered. |
### Metered() {#Metered}
```
public Metered()
```


Инициализирует новый экземпляр этого класса.

 **Examples:** 

Показывает, как активировать Metered‑лицензию и отслеживать кредит/потребление.

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


Получает кредит потребления

 **Examples:** 

Показывает, как активировать Metered‑лицензию и отслеживать кредит/потребление.

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
java.math.BigDecimal - количество потребления
### getConsumptionQuantity() {#getConsumptionQuantity}
```
public static BigDecimal getConsumptionQuantity()
```


Получает размер файла потребления

 **Examples:** 

Показывает, как активировать Metered‑лицензию и отслеживать кредит/потребление.

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
java.math.BigDecimal - количество потребления
### getProductName() {#getProductName}
```
public String getProductName()
```


Возвращает название продукта

 **Examples:** 

Показывает, как активировать Metered‑лицензию и отслеживать кредит/потребление.

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
java.lang.String - название продукта
### isMeteredLicensed() {#isMeteredLicensed}
```
public static boolean isMeteredLicensed()
```


Проверяет, лицензирована ли Metered

 **Examples:** 

Показывает, как активировать Metered‑лицензию и отслеживать кредит/потребление.

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
boolean - Истина или ложь
### setMeteredKey(String publicKey, String privateKey) {#setMeteredKey-java.lang.String-java.lang.String}
```
public void setMeteredKey(String publicKey, String privateKey)
```


Устанавливает измеряемый публичный и приватный ключ. Если вы приобретаете измеряемую лицензию, при запуске приложения этот API должен быть вызван, обычно этого достаточно. Однако, если постоянно не удаётся загрузить данные о потреблении и прошло более 24 часов, лицензия будет переведена в статус оценки; чтобы избежать этого, следует регулярно проверять статус лицензии, и если он находится в статусе оценки, вызвать этот API снова.

 **Examples:** 

Показывает, как активировать Metered‑лицензию и отслеживать кредит/потребление.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| publicKey | java.lang.String | публичный ключ |
| privateKey | java.lang.String | приватный ключ |

