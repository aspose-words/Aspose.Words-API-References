---
title: Font.StyleName
linktitle: StyleName
articleTitle: StyleName
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font StyleName, легко управляйте стилями символов для улучшенного форматирования текста и гибкости дизайна в ваших проектах.
type: docs
weight: 430
url: /ru/net/aspose.words/font/stylename/
---
## Font.StyleName property

Возвращает или задает имя стиля символа, примененного к данному форматированию.

```csharp
public string StyleName { get; set; }
```

## Примеры

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

// Преобразовать все использования одного стиля в другой,
// используем вышеуказанные методы для ссылки на старые и новые стили.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true))
{
    if (run.Font.StyleName == "Emphasis")
        run.Font.StyleName = "Strong";

    if (run.Font.StyleIdentifier == StyleIdentifier.IntenseEmphasis)
        run.Font.StyleIdentifier = StyleIdentifier.Strong;
}

doc.Save(ArtifactsDir + "Font.ChangeStyle.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
