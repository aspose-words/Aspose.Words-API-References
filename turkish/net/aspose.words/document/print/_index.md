---
title: Print
second_title: Aspose.Words for .NET API Referansı
description: Belgenin tamamını varsayılan yazıcıya yazdırır.
type: docs
weight: 620
url: /tr/net/aspose.words/document/print/
---
## Print() {#print}

Belgenin tamamını varsayılan yazıcıya yazdırır.

```csharp
public void Print()
```

### Örnekler

Varsayılan yazıcıyı kullanarak bir belgenin nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Aşağıda belgemizi yazdırmanın iki yolu bulunmaktadır.
// 1 - Varsayılan yazıcıyı kullanarak yazdırın:
doc.Print();

// 2 - Belgeyi yazdırmak istediğimiz yazıcıyı adıyla belirtin:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)

---

## Print(string) {#print_3}

Standart (Kullanıcı Arayüzü yok) yazdırma denetleyicisini kullanarak tüm belgeyi belirtilen yazıcıya yazdırın, .

```csharp
public void Print(string printerName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| printerName | String | Yazıcının adı. |

### Örnekler

Varsayılan yazıcıyı kullanarak bir belgenin nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Aşağıda belgemizi yazdırmanın iki yolu bulunmaktadır.
// 1 - Varsayılan yazıcıyı kullanarak yazdırın:
doc.Print();

// 2 - Belgeyi yazdırmak istediğimiz yazıcıyı adıyla belirtin:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)

---

## Print(PrinterSettings) {#print_1}

Belgeyi belirtilen yazıcı ayarlarına göre yazdırır, standart (Kullanıcı Arayüzü yok) yazdırma denetleyicisini kullanarak.

```csharp
public void Print(PrinterSettings printerSettings)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| printerSettings | PrinterSettings | Kullanılacak yazıcı ayarları. |

### Notlar

buPrinterSettings nesnesi, yazdırılacak yazıcıyı, yazdırılacak sayfa aralığını ve diğer seçenekleri belirlemenizi sağlar.

### Örnekler

Bir dizi sayfanın nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Belgeyi nasıl yazdıracağımızı değiştirmek için bir "PrinterSettings" nesnesi oluşturun.
PrinterSettings printerSettings = new PrinterSettings();

// "PrintRange" özelliğini "PrintRange.SomePages" olarak ayarlayın.
// yazıcıya yalnızca bazı belge sayfalarını yazdırmayı planladığımızı söyleyin.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// 1'den 3'e kadar olan sayfaları yazdırmak için "FromPage" özelliğini "1" ve "ToPage" özelliğini "3" olarak ayarlayın.
// Sayfa indeksleme 1 tabanlıdır.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Aşağıda belgemizi yazdırmanın iki yolu bulunmaktadır.
// 1 - Yazdırma ayarlarımızı uygularken yazdırın:
doc.Print(printerSettings);

// 2 - Yazdırma ayarlarımızı uygularken yazdırın, aynı zamanda
// belgeye yazıcı kuyruğunda tanıyabileceğimiz özel bir ad vererek:
doc.Print(printerSettings, "My rendered document");
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)

---

## Print(PrinterSettings, string) {#print_2}

Belgeyi belirtilen yazıcı ayarlarına göre yazdırır, standart (Kullanıcı Arayüzü yok) yazdırma denetleyicisini ve bir belge adını kullanarak.

```csharp
public void Print(PrinterSettings printerSettings, string documentName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| printerSettings | PrinterSettings | Kullanılacak yazıcı ayarları. |
| documentName | String | Belge yazdırılırken görüntülenecek belge adı (örneğin, bir yazdırma durumu iletişim kutusunda veya yazıcı kuyruğunda). |

### Notlar

buPrinterSettings nesnesi, yazdırılacak yazıcıyı, yazdırılacak sayfa aralığını ve diğer seçenekleri belirlemenizi sağlar.

### Örnekler

Bir dizi sayfanın nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Belgeyi nasıl yazdıracağımızı değiştirmek için bir "PrinterSettings" nesnesi oluşturun.
PrinterSettings printerSettings = new PrinterSettings();

// "PrintRange" özelliğini "PrintRange.SomePages" olarak ayarlayın.
// yazıcıya yalnızca bazı belge sayfalarını yazdırmayı planladığımızı söyleyin.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// 1'den 3'e kadar olan sayfaları yazdırmak için "FromPage" özelliğini "1" ve "ToPage" özelliğini "3" olarak ayarlayın.
// Sayfa indeksleme 1 tabanlıdır.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Aşağıda belgemizi yazdırmanın iki yolu bulunmaktadır.
// 1 - Yazdırma ayarlarımızı uygularken yazdırın:
doc.Print(printerSettings);

// 2 - Yazdırma ayarlarımızı uygularken yazdırın, aynı zamanda
// belgeye yazıcı kuyruğunda tanıyabileceğimiz özel bir ad vererek:
doc.Print(printerSettings, "My rendered document");
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
