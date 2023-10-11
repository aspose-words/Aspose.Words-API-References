---
title: Font.NameOther
second_title: Справочник по API Aspose.Words для .NET
description: Font свойство. Возвращает или задает шрифт используемый для символов с кодами символов от 128 до 255.
type: docs
weight: 270
url: /ru/net/aspose.words/font/nameother/
---
## Font.NameOther property

Возвращает или задает шрифт, используемый для символов с кодами символов от 128 до 255.

```csharp
public string NameOther { get; set; }
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


