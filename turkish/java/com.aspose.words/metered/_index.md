---
title: "Metered"
linktitle: "Metered"
second_title: "Aspose.Words Java için"
description: "Java'da ölçümlü anahtarı ayarlamak için yöntemler sağlar."
type: docs
weight: 469
url: /tr/java/com.aspose.words/metered/
---

**Inheritance:**
java.lang.Object
```
public class Metered
```

Ölçülen anahtarı ayarlamak için yöntemler sağlar.

 **Examples:** 

Ölçümlü bir lisansı etkinleştirme ve kredi/tüketimi izleme yöntemini gösterir.

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
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [Metered()](#Metered) | Bu sınıfın yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getConsumptionCredit()](#getConsumptionCredit) | Tüketim kredisini alır |
| [getConsumptionQuantity()](#getConsumptionQuantity) | Tüketim dosya boyutunu alır |
| [getProductName()](#getProductName) | Ürün adını döndürür |
| [isMeteredLicensed()](#isMeteredLicensed) | Ölçümlünün lisanslı olup olmadığını kontrol eder |
| [setMeteredKey(String publicKey, String privateKey)](#setMeteredKey-java.lang.String-java.lang.String) | Ölçümlü genel ve özel anahtarı ayarlar. |
### Metered() {#Metered}
```
public Metered()
```


Bu sınıfın yeni bir örneğini başlatır.

 **Examples:** 

Ölçümlü bir lisansı etkinleştirme ve kredi/tüketimi izleme yöntemini gösterir.

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


Tüketim kredisini alır

 **Examples:** 

Ölçümlü bir lisansı etkinleştirme ve kredi/tüketimi izleme yöntemini gösterir.

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
java.math.BigDecimal - tüketim miktarı
### getConsumptionQuantity() {#getConsumptionQuantity}
```
public static BigDecimal getConsumptionQuantity()
```


Tüketim dosya boyutunu alır

 **Examples:** 

Ölçümlü bir lisansı etkinleştirme ve kredi/tüketimi izleme yöntemini gösterir.

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
java.math.BigDecimal - tüketim miktarı
### getProductName() {#getProductName}
```
public String getProductName()
```


Ürün adını döndürür

 **Examples:** 

Ölçümlü bir lisansı etkinleştirme ve kredi/tüketimi izleme yöntemini gösterir.

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
java.lang.String - Ürün adı
### isMeteredLicensed() {#isMeteredLicensed}
```
public static boolean isMeteredLicensed()
```


Ölçümlünün lisanslı olup olmadığını kontrol eder

 **Examples:** 

Ölçümlü bir lisansı etkinleştirme ve kredi/tüketimi izleme yöntemini gösterir.

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
boolean - Doğru veya yanlış
### setMeteredKey(String publicKey, String privateKey) {#setMeteredKey-java.lang.String-java.lang.String}
```
public void setMeteredKey(String publicKey, String privateKey)
```


Ölçülen genel ve özel anahtarı ayarlar. Ölçülen lisansı satın alırsanız, uygulamayı başlattığınızda bu API çağrılmalıdır, genellikle bu yeterlidir. Ancak, tüketim verilerini yüklemeyi sürekli olarak başaramaz ve 24 saat aşarsa, lisans değerlendirme durumuna ayarlanır; böyle bir durumu önlemek için lisans durumunu düzenli olarak kontrol etmelisiniz, eğer değerlendirme durumundaysa, bu API'yi tekrar çağırın.

 **Examples:** 

Ölçümlü bir lisansı etkinleştirme ve kredi/tüketimi izleme yöntemini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| publicKey | java.lang.String | genel anahtar |
| privateKey | java.lang.String | özel anahtar |

