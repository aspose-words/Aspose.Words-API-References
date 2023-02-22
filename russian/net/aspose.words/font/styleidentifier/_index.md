---
title: Font.StyleIdentifier
second_title: Справочник по API Aspose.Words для .NET
description: Font свойство. Получает или задает независимый от языкового стандарта идентификатор стиля символа примененного к данному форматированию.
type: docs
weight: 410
url: /ru/net/aspose.words/font/styleidentifier/
---
## Font.StyleIdentifier property

Получает или задает независимый от языкового стандарта идентификатор стиля символа, примененного к данному форматированию.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

### Примеры

Показывает, как изменить стиль существующего текста.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два способа ссылки на стили.
// 1 - Использование имени стиля:
builder.Font.StyleName = "Emphasis";
builder.Writeln("Text originally in \"Emphasis\" style");

// 2 - Использование встроенного идентификатора стиля:
builder.Font.StyleIdentifier = StyleIdentifier.IntenseEmphasis;
builder.Writeln("Text originally in \"Intense Emphasis\" style");

// Преобразование всех использований одного стиля в другой,
// используя вышеуказанные методы для ссылки на старый и новый стили.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true).OfType<Run>())
{
    if (run.Font.StyleName == "Emphasis")
        run.Font.StyleName = "Strong";

    if (run.Font.StyleIdentifier == StyleIdentifier.IntenseEmphasis)
        run.Font.StyleIdentifier = StyleIdentifier.Strong;
}

doc.Save(ArtifactsDir + "Font.ChangeStyle.docx");
```

### Смотрите также

* enum [StyleIdentifier](../../styleidentifier/)
* class [Font](../)
* пространство имен [Aspose.Words](../../font/)
* сборка [Aspose.Words](../../../)


