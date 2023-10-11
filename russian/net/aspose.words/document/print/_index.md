---
title: Document.Print
second_title: Справочник по API Aspose.Words для .NET
description: Document метод. Печатает весь документ на принтере по умолчанию.
type: docs
weight: 660
url: /ru/net/aspose.words/document/print/
---
## Print() {#print}

Печатает весь документ на принтере по умолчанию.

```csharp
public void Print()
```

### Примеры

Показывает, как распечатать документ с помощью принтера по умолчанию.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Ниже приведены два способа печати нашего документа.
// 1 - Печать с использованием принтера по умолчанию:
doc.Print();

// 2 - Указываем принтер, на котором хотим распечатать документ, по имени:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)

---

## Print(string) {#print_3}

Распечатайте весь документ на указанном принтере, , используя стандартный контроллер печати (без пользовательского интерфейса).

```csharp
public void Print(string printerName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| printerName | String | Имя принтера. |

### Примеры

Показывает, как распечатать документ с помощью принтера по умолчанию.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Ниже приведены два способа печати нашего документа.
// 1 - Печать с использованием принтера по умолчанию:
doc.Print();

// 2 - Указываем принтер, на котором хотим распечатать документ, по имени:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)

---

## Print(PrinterSettings) {#print_1}

Печатает документ в соответствии с указанными настройками принтера, с использованием стандартного (без пользовательского интерфейса) контроллера печати.

```csharp
public void Print(PrinterSettings printerSettings)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| printerSettings | PrinterSettings | Используемые настройки принтера. |

### Примечания

PrinterSettings Объект позволяет указать принтер для печати, диапазон страниц для печати и другие параметры.

### Примеры

Показывает, как распечатать диапазон страниц.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Создайте объект PrinterSettings, чтобы изменить способ печати документа.
PrinterSettings printerSettings = new PrinterSettings();

// Установите для свойства PrintRange значение PrintRange.SomePages, чтобы
// сообщаем принтеру, что мы намерены распечатать только некоторые страницы документа.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// Установите для свойства FromPage значение «1», а для свойства ToPage — значение «3», чтобы напечатать страницы с 1 по 3.
// Индексация страницы начинается с 1.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Ниже приведены два способа печати нашего документа.
// 1 — Печать с применением наших настроек печати:
doc.Print(printerSettings);

// 2 — Печать с применением наших настроек печати, а также
// присвоение документу специального имени, которое мы можем распознать в очереди принтера:
doc.Print(printerSettings, "My rendered document");
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)

---

## Print(PrinterSettings, string) {#print_2}

Печатает документ в соответствии с указанными настройками принтера, с использованием стандартного контроллера печати (без пользовательского интерфейса) и имени документа.

```csharp
public void Print(PrinterSettings printerSettings, string documentName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| printerSettings | PrinterSettings | Используемые настройки принтера. |
| documentName | String | Имя документа, которое будет отображаться (например, в диалоговом окне состояния печати или в очереди принтера) при печати документа. |

### Примечания

PrinterSettings Объект позволяет указать принтер для печати, диапазон страниц для печати и другие параметры.

### Примеры

Показывает, как распечатать диапазон страниц.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Создайте объект PrinterSettings, чтобы изменить способ печати документа.
PrinterSettings printerSettings = new PrinterSettings();

// Установите для свойства PrintRange значение PrintRange.SomePages, чтобы
// сообщаем принтеру, что мы намерены распечатать только некоторые страницы документа.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// Установите для свойства FromPage значение «1», а для свойства ToPage — значение «3», чтобы напечатать страницы с 1 по 3.
// Индексация страницы начинается с 1.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Ниже приведены два способа печати нашего документа.
// 1 — Печать с применением наших настроек печати:
doc.Print(printerSettings);

// 2 — Печать с применением наших настроек печати, а также
// присвоение документу специального имени, которое мы можем распознать в очереди принтера:
doc.Print(printerSettings, "My rendered document");
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


