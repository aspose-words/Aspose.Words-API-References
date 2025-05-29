---
title: Font.Emboss
linktitle: Emboss
articleTitle: Emboss
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font Emboss, которое улучшает ваш текст стильным эффектом тиснения для создания привлекательных дизайнов. Поднимите свою типографику сегодня!
type: docs
weight: 100
url: /ru/net/aspose.words/font/emboss/
---
## Font.Emboss property

True, если шрифт отформатирован как рельефный.

```csharp
public bool Emboss { get; set; }
```

## Примеры

Показывает, как применять эффекты гравировки/тиснения к тексту.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Color = Color.LightBlue;

// Ниже приведены два способа использования теней для создания 3D-эффекта в тексте.
// 1 - Выгравируйте текст так, чтобы буквы выглядели утопленными в страницу:
builder.Font.Engrave = true;

builder.Writeln("This text is engraved.");

// 2 - Выдавите текст, чтобы буквы выглядели так, будто выступают из страницы:
builder.Font.Engrave = false;
builder.Font.Emboss = true;

builder.Writeln("This text is embossed.");

doc.Save(ArtifactsDir + "Font.EngraveEmboss.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
