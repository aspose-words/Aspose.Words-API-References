---
title: Document.Print
linktitle: Print
articleTitle: Print
second_title: .NET için Aspose.Words
description: Sorunsuz Belge Yazdırma yöntemimizle tüm belgenizi varsayılan yazıcınıza zahmetsizce yazdırın. Hızlı, zahmetsiz yazdırmanın tadını çıkarın!
type: docs
weight: 680
url: /tr/net/aspose.words/document/print/
---
## Print() {#print}

Tüm belgeyi varsayılan yazıcıya yazdırır.

```csharp
public void Print()
```

## Örnekler

Varsayılan yazıcıyı kullanarak bir belgenin nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Aşağıda belgemizi yazdırmanın iki yolu bulunmaktadır.
// 1 - Varsayılan yazıcıyı kullanarak yazdır:
doc.Print();

// 2 - Belgeyi yazdırmak istediğimiz yazıcıyı adıyla belirtin:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Print(*string*) {#print_3}

Tüm belgeyi belirtilen yazıcıya yazdırın, standart (Kullanıcı Arayüzü yok) yazdırma denetleyicisini kullanarak.

```csharp
public void Print(string printerName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| printerName | String | Yazıcının adı. |

## Örnekler

Varsayılan yazıcıyı kullanarak bir belgenin nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Aşağıda belgemizi yazdırmanın iki yolu bulunmaktadır.
// 1 - Varsayılan yazıcıyı kullanarak yazdır:
doc.Print();

// 2 - Belgeyi yazdırmak istediğimiz yazıcıyı adıyla belirtin:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Print(*PrinterSettings*) {#print_1}

Belgeyi belirtilen yazıcı ayarlarına göre yazdırır, standart (Kullanıcı Arayüzü yok) yazdırma denetleyicisini kullanarak.

```csharp
public void Print(PrinterSettings printerSettings)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| printerSettings | PrinterSettings | Kullanılacak yazıcı ayarları. |

## Notlar

ThePrinterSettings nesnesi, üzerine yazdırılacak yazıcıyı, yazdırılacak sayfa aralığını ve diğer seçenekleri belirtmenize olanak tanır.

## Örnekler

Bir dizi sayfanın nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Belgeyi nasıl yazdıracağımızı değiştirmek için bir "PrinterSettings" nesnesi oluşturun.
PrinterSettings printerSettings = new PrinterSettings();

// "PrintRange" özelliğini "PrintRange.SomePages" olarak ayarlayın
// yazıcıya yalnızca bazı belge sayfalarını yazdırmak istediğimizi söyleriz.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// 1'den 3'e kadar olan sayfaları yazdırmak için "FromPage" özelliğini "1", "ToPage" özelliğini ise "3" olarak ayarlayın.
// Sayfa indekslemesi 1 tabanlıdır.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Aşağıda belgemizi yazdırmanın iki yolu bulunmaktadır.
// 1 - Yazdırma ayarlarımızı uygulayarak yazdıralım:
doc.Print(printerSettings);

// 2 - Yazdırma ayarlarımızı uygularken yazdırın, aynı zamanda
// belgeye yazıcı kuyruğunda tanıyabileceğimiz özel bir ad veriyoruz:
doc.Print(printerSettings, "My rendered document");
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Print(*PrinterSettings, string*) {#print_2}

Standart (Kullanıcı Arayüzü yok) yazdırma denetleyicisini ve bir belge adını kullanarak, belirtilen yazıcı ayarlarına göre belgeyi yazdırır.

```csharp
public void Print(PrinterSettings printerSettings, string documentName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| printerSettings | PrinterSettings | Kullanılacak yazıcı ayarları. |
| documentName | String | Belge yazdırılırken görüntülenecek belge adı (örneğin, yazdırma durumu iletişim kutusu kutusunda veya yazıcı kuyruğunda). |

## Notlar

ThePrinterSettings nesnesi, üzerine yazdırılacak yazıcıyı, yazdırılacak sayfa aralığını ve diğer seçenekleri belirtmenize olanak tanır.

## Örnekler

Bir dizi sayfanın nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Belgeyi nasıl yazdıracağımızı değiştirmek için bir "PrinterSettings" nesnesi oluşturun.
PrinterSettings printerSettings = new PrinterSettings();

// "PrintRange" özelliğini "PrintRange.SomePages" olarak ayarlayın
// yazıcıya yalnızca bazı belge sayfalarını yazdırmak istediğimizi söyleriz.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// 1'den 3'e kadar olan sayfaları yazdırmak için "FromPage" özelliğini "1", "ToPage" özelliğini ise "3" olarak ayarlayın.
// Sayfa indekslemesi 1 tabanlıdır.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Aşağıda belgemizi yazdırmanın iki yolu bulunmaktadır.
// 1 - Yazdırma ayarlarımızı uygulayarak yazdıralım:
doc.Print(printerSettings);

// 2 - Yazdırma ayarlarımızı uygularken yazdırın, aynı zamanda
// belgeye yazıcı kuyruğunda tanıyabileceğimiz özel bir ad veriyoruz:
doc.Print(printerSettings, "My rendered document");
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
