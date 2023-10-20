---
title: Font.Engrave
linktitle: Engrave
articleTitle: Engrave
second_title: Aspose.Words для .NET
description: Font Engrave свойство. True если шрифт отформатирован как гравированный на С#.
type: docs
weight: 120
url: /ru/net/aspose.words/font/engrave/
---
## Font.Engrave property

True, если шрифт отформатирован как гравированный.

```csharp
public bool Engrave { get; set; }
```

## Примеры

Показывает, как применять эффекты гравировки/тиснения к тексту.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Color = Color.LightBlue;

// Ниже приведены два способа использования теней для применения к тексту трехмерного эффекта.
// 1 — Выгравировать текст, чтобы он выглядел так, как будто буквы утоплены в странице:
builder.Font.Engrave = true;

builder.Writeln("This text is engraved.");

// 2 — Тиснение текста, чтобы оно выглядело так, будто буквы выскакивают из страницы:
builder.Font.Engrave = false;
builder.Font.Emboss = true;

builder.Writeln("This text is embossed.");

doc.Save(ArtifactsDir + "Font.EngraveEmboss.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
