---
title: Font.NameOther
linktitle: NameOther
articleTitle: NameOther
second_title: Aspose.Words для .NET
description: Откройте для себя Font NameOther. Легко настраивайте шрифты для кодов символов 128-255, улучшая стиль и читаемость вашего текста. Поднимите свой дизайн сегодня!
type: docs
weight: 270
url: /ru/net/aspose.words/font/nameother/
---
## Font.NameOther property

Возвращает или задает шрифт, используемый для символов с кодами от 128 до 255.

```csharp
public string NameOther { get; set; }
```

## Примеры

Демонстрирует, как Microsoft Word может объединить два разных шрифта за один запуск.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Предположим, что мы используем конструктор для вставки, используя эту конфигурацию шрифта
// содержит символы в диапазоне символов ASCII. В этом случае,
// он отобразит эти символы, используя этот шрифт.
builder.Font.NameAscii = "Calibri";

// Если другой шрифт не указан, конструктор также применит этот шрифт ко всем вставляемым им символам.
Assert.AreEqual("Calibri", builder.Font.Name);

// Укажите шрифт, который будет использоваться для всех символов за пределами диапазона ASCII.
// В идеале этот шрифт должен иметь глиф для каждого требуемого кода символа, не входящего в ASCII.
builder.Font.NameOther = "Courier New";

// Вставьте последовательность из одного слова, состоящего из символов ASCII, и одного слова, содержащего все символы за пределами этого диапазона.
// Каждый символ будет отображаться с использованием одного из шрифтов, в зависимости от.
builder.Writeln("Hello, Привет");

doc.Save(ArtifactsDir + "Font.NameAscii.docx");
```

### Смотрите также

* property [Name](../name/)
* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
