---
title: Font.NameAscii
second_title: Справочник по API Aspose.Words для .NET
description: Font свойство. Возвращает или задает шрифт используемый для латинского текста символы с кодами символов от 0 нуля до 127.
type: docs
weight: 240
url: /ru/net/aspose.words/font/nameascii/
---
## Font.NameAscii property

Возвращает или задает шрифт, используемый для латинского текста (символы с кодами символов от 0 (нуля) до 127).

```csharp
public string NameAscii { get; set; }
```

### Примеры

Показывает, как Microsoft Word может комбинировать два разных шрифта за один проход.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Предположим, что мы используем построитель для вставки при использовании этой конфигурации шрифта
// содержит символы в диапазоне символов ASCII. В таком случае,
// эти символы будут отображаться с использованием этого шрифта.
builder.Font.NameAscii = "Calibri";

// Если не указан другой шрифт, конструктор также будет применять этот шрифт ко всем вставляемым символам.
Assert.AreEqual("Calibri", builder.Font.Name);

// Укажите шрифт, который будет использоваться для всех символов за пределами диапазона ASCII.
// В идеале этот шрифт должен иметь глиф для каждого требуемого кода символа, отличного от ASCII.
builder.Font.NameOther = "Courier New";

// Вставьте серию с одним словом, состоящим из символов ASCII, и одним словом со всеми символами вне этого диапазона.
// Каждый символ будет отображаться с использованием любого из шрифтов, в зависимости от.
builder.Writeln("Hello, Привет");

doc.Save(ArtifactsDir + "Font.NameAscii.docx");
```

### Смотрите также

* property [Name](../name/)
* class [Font](../)
* пространство имен [Aspose.Words](../../font/)
* сборка [Aspose.Words](../../../)


