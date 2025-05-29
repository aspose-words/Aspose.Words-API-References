---
title: Font.NameAscii
linktitle: NameAscii
articleTitle: NameAscii
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font NameAscii для настройки латинских текстовых шрифтов, дополнив свой дизайн кодами символов 0–127 для улучшения читаемости.
type: docs
weight: 240
url: /ru/net/aspose.words/font/nameascii/
---
## Font.NameAscii property

Возвращает или задает шрифт, используемый для латинского текста (символы с кодами символов от 0 (нуля) до 127).

```csharp
public string NameAscii { get; set; }
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
