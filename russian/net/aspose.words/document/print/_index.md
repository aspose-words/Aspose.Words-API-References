---
title: Document.Print
linktitle: Print
articleTitle: Print
second_title: Aspose.Words для .NET
description: Легко распечатайте весь документ на принтере по умолчанию с помощью нашего оптимизированного метода Document Print. Наслаждайтесь быстрой и беспроблемной печатью!
type: docs
weight: 680
url: /ru/net/aspose.words/document/print/
---
## Print() {#print}

Печатает весь документ на принтере по умолчанию.

```csharp
public void Print()
```

## Примеры

Показывает, как распечатать документ с помощью принтера по умолчанию.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Ниже приведены два способа печати нашего документа.
// 1 — Печать с использованием принтера по умолчанию:
doc.Print();

// 2 - Указываем имя принтера, на котором мы хотим распечатать документ:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## Print(*string*) {#print_3}

Распечатать весь документ на указанном принтере, используя стандартный (без пользовательского интерфейса) контроллер печати.

```csharp
public void Print(string printerName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| printerName | String | Название принтера. |

## Примеры

Показывает, как распечатать документ с помощью принтера по умолчанию.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Ниже приведены два способа печати нашего документа.
// 1 — Печать с использованием принтера по умолчанию:
doc.Print();

// 2 - Указываем имя принтера, на котором мы хотим распечатать документ:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## Print(*PrinterSettings*) {#print_1}

Печатает документ в соответствии с указанными настройками принтера, используя стандартный (без пользовательского интерфейса) контроллер печати.

```csharp
public void Print(PrinterSettings printerSettings)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| printerSettings | PrinterSettings | Настройки принтера, которые необходимо использовать. |

## Примечания

ThePrinterSettings Объект позволяет указать принтер для печати, диапазон страниц для печати и другие параметры.

## Примеры

Показывает, как распечатать ряд страниц.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Создаем объект «PrinterSettings» для изменения способа печати документа.
PrinterSettings printerSettings = new PrinterSettings();

// Установите свойство "PrintRange" на "PrintRange.SomePages" для
// сообщаем принтеру, что мы собираемся напечатать только некоторые страницы документа.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// Установите свойство «FromPage» на «1», а свойство «ToPage» на «3», чтобы напечатать страницы с 1 по 3.
// Индексация страниц начинается с 1.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Ниже приведены два способа печати нашего документа.
// 1 — Печать с применением наших настроек печати:
doc.Print(printerSettings);

// 2 - Печать с применением наших настроек печати, а также
// присваиваем документу имя, которое мы сможем распознать в очереди печати:
doc.Print(printerSettings, "My rendered document");
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## Print(*PrinterSettings, string*) {#print_2}

Печатает документ в соответствии с указанными настройками принтера, используя стандартный (без пользовательского интерфейса) контроллер печати и имя документа.

```csharp
public void Print(PrinterSettings printerSettings, string documentName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| printerSettings | PrinterSettings | Настройки принтера, которые необходимо использовать. |
| documentName | String | Имя документа, которое будет отображаться (например, в окне состояния печати dialog или в очереди принтера) при печати документа. |

## Примечания

ThePrinterSettings Объект позволяет указать принтер для печати, диапазон страниц для печати и другие параметры.

## Примеры

Показывает, как распечатать ряд страниц.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Создаем объект «PrinterSettings» для изменения способа печати документа.
PrinterSettings printerSettings = new PrinterSettings();

// Установите свойство "PrintRange" на "PrintRange.SomePages" для
// сообщаем принтеру, что мы собираемся напечатать только некоторые страницы документа.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// Установите свойство «FromPage» на «1», а свойство «ToPage» на «3», чтобы напечатать страницы с 1 по 3.
// Индексация страниц начинается с 1.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Ниже приведены два способа печати нашего документа.
// 1 — Печать с применением наших настроек печати:
doc.Print(printerSettings);

// 2 - Печать с применением наших настроек печати, а также
// присваиваем документу имя, которое мы сможем распознать в очереди печати:
doc.Print(printerSettings, "My rendered document");
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
