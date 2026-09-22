---
title: "Metered"
linktitle: "Metered"
second_title: "Aspose.Words لـ Java"
description: "يوفر طرقًا لتعيين المفتاح المقيس في Java."
type: docs
weight: 469
url: /ar/java/com.aspose.words/metered/
---

**Inheritance:**
java.lang.Object
```
public class Metered
```

يوفر طرقًا لتعيين المفتاح المقاس.

 **Examples:** 

يوضح كيفية تفعيل ترخيص Metered وتتبع الائتمان/الاستهلاك.

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
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [Metered()](#Metered) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getConsumptionCredit()](#getConsumptionCredit) | يحصل على رصيد الاستهلاك |
| [getConsumptionQuantity()](#getConsumptionQuantity) | يحصل على حجم ملف الاستهلاك |
| [getProductName()](#getProductName) | يرجع اسم المنتج |
| [isMeteredLicensed()](#isMeteredLicensed) | تحقق مما إذا كان Metered مرخصًا |
| [setMeteredKey(String publicKey, String privateKey)](#setMeteredKey-java.lang.String-java.lang.String) | يضبط المفتاح العام والخاص لـ Metered. |
### Metered() {#Metered}
```
public Metered()
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

 **Examples:** 

يوضح كيفية تفعيل ترخيص Metered وتتبع الائتمان/الاستهلاك.

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


يحصل على رصيد الاستهلاك

 **Examples:** 

يوضح كيفية تفعيل ترخيص Metered وتتبع الائتمان/الاستهلاك.

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
java.math.BigDecimal - كمية الاستهلاك
### getConsumptionQuantity() {#getConsumptionQuantity}
```
public static BigDecimal getConsumptionQuantity()
```


يحصل على حجم ملف الاستهلاك

 **Examples:** 

يوضح كيفية تفعيل ترخيص Metered وتتبع الائتمان/الاستهلاك.

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
java.math.BigDecimal - كمية الاستهلاك
### getProductName() {#getProductName}
```
public String getProductName()
```


يرجع اسم المنتج

 **Examples:** 

يوضح كيفية تفعيل ترخيص Metered وتتبع الائتمان/الاستهلاك.

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
java.lang.String - اسم المنتج
### isMeteredLicensed() {#isMeteredLicensed}
```
public static boolean isMeteredLicensed()
```


تحقق مما إذا كان Metered مرخصًا

 **Examples:** 

يوضح كيفية تفعيل ترخيص Metered وتتبع الائتمان/الاستهلاك.

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
boolean - صحيح أو خطأ
### setMeteredKey(String publicKey, String privateKey) {#setMeteredKey-java.lang.String-java.lang.String}
```
public void setMeteredKey(String publicKey, String privateKey)
```


يضبط المفتاح العام والخاص القابل للقياس. إذا قمت بشراء ترخيص قابل للقياس، عند بدء التطبيق يجب استدعاء هذه الواجهة البرمجية (API)، عادةً يكون ذلك كافياً. ومع ذلك، إذا فشل دائمًا تحميل بيانات الاستهلاك وتجاوز 24 ساعة، سيتم تعيين الترخيص إلى حالة التقييم؛ لتجنب هذه الحالة، يجب عليك فحص حالة الترخيص بانتظام، إذا كانت في حالة التقييم، استدعِ هذه الواجهة البرمجية مرة أخرى.

 **Examples:** 

يوضح كيفية تفعيل ترخيص Metered وتتبع الائتمان/الاستهلاك.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| publicKey | java.lang.String | المفتاح العام |
| privateKey | java.lang.String | المفتاح الخاص |

