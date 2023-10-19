---
title: Document.Print
linktitle: Print
articleTitle: Print
second_title: Aspose.Words for .NET
description: Document Print yöntem. Belgenin tamamını varsayılan yazıcıya yazdırır C#'da.
type: docs
weight: 640
url: /tr/net/aspose.words/document/print/
---
## Print() {#print}

Belgenin tamamını varsayılan yazıcıya yazdırır.

```csharp
public void Print()
```

## Örnekler

Varsayılan yazıcıyı kullanarak bir belgenin nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Aşağıda belgemizi yazdırmanın iki yolu verilmiştir.
// 1 - Varsayılan yazıcıyı kullanarak yazdırın:
doc.Print();

// 2 - Belgeyi adıyla yazdırmak istediğimiz yazıcıyı belirtin:
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

Standart (Kullanıcı Arayüzü olmayan) yazdırma denetleyicisini kullanarak belgenin tamamını belirtilen yazıcıya, yazdırın.

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

// Aşağıda belgemizi yazdırmanın iki yolu verilmiştir.
// 1 - Varsayılan yazıcıyı kullanarak yazdırın:
doc.Print();

// 2 - Belgeyi adıyla yazdırmak istediğimiz yazıcıyı belirtin:
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

Belgeyi belirtilen yazıcı ayarlarına göre standart (Kullanıcı Arayüzü yok) yazdırma denetleyicisini kullanarak yazdırır.

```csharp
public void Print(PrinterSettings printerSettings)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| printerSettings | PrinterSettings | Kullanılacak yazıcı ayarları. |

## Notlar

PrinterSettings nesnesi, yazdırılacak yazıcıyı, yazdırılacak sayfa aralığını ve diğer seçenekleri belirtmenize olanak tanır.

## Örnekler

Bir dizi sayfanın nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Belgeyi yazdırma şeklimizi değiştirmek için bir "PrinterSettings" nesnesi oluşturun.
PrinterSettings printerSettings = new PrinterSettings();

// "PrintRange" özelliğini "PrintRange.SomePages" olarak ayarlayın.
// yazıcıya yalnızca bazı belge sayfalarını yazdırmak istediğimizi söyleyin.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// 1'den 3'e kadar olan sayfaları yazdırmak için "FromPage" özelliğini "1" ve "ToPage" özelliğini "3" olarak ayarlayın.
// Sayfa indeksleme 1 tabanlıdır.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Aşağıda belgemizi yazdırmanın iki yolu verilmiştir.
// 1 - Yazdırma ayarlarımızı uygulayarak yazdırın:
doc.Print(printerSettings);

// 2 - Yazdırma ayarlarımızı uygularken aynı zamanda yazdırın
// belgeye yazıcı kuyruğunda tanıyabileceğimiz özel bir ad veriyoruz:
doc.Print(printerSettings, "My rendered document");
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Print(*PrinterSettings, string*) {#print_2}

Belgeyi belirtilen yazıcı ayarlarına göre standart (Kullanıcı Arayüzü yok) yazdırma denetleyicisini ve belge adını kullanarak yazdırır.

```csharp
public void Print(PrinterSettings printerSettings, string documentName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| printerSettings | PrinterSettings | Kullanılacak yazıcı ayarları. |
| documentName | String | Belgeyi yazdırırken görüntülenecek belge adı (örneğin, yazdırma durumu iletişim kutusunda kutusunda veya yazıcı kuyruğunda). |

## Notlar

PrinterSettings nesnesi, yazdırılacak yazıcıyı, yazdırılacak sayfa aralığını ve diğer seçenekleri belirtmenize olanak tanır.

## Örnekler

Bir dizi sayfanın nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Belgeyi yazdırma şeklimizi değiştirmek için bir "PrinterSettings" nesnesi oluşturun.
PrinterSettings printerSettings = new PrinterSettings();

// "PrintRange" özelliğini "PrintRange.SomePages" olarak ayarlayın.
// yazıcıya yalnızca bazı belge sayfalarını yazdırmak istediğimizi söyleyin.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// 1'den 3'e kadar olan sayfaları yazdırmak için "FromPage" özelliğini "1" ve "ToPage" özelliğini "3" olarak ayarlayın.
// Sayfa indeksleme 1 tabanlıdır.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Aşağıda belgemizi yazdırmanın iki yolu verilmiştir.
// 1 - Yazdırma ayarlarımızı uygulayarak yazdırın:
doc.Print(printerSettings);

// 2 - Yazdırma ayarlarımızı uygularken aynı zamanda yazdırın
// belgeye yazıcı kuyruğunda tanıyabileceğimiz özel bir ad veriyoruz:
doc.Print(printerSettings, "My rendered document");
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
