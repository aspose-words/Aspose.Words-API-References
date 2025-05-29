---
title: Dml3DEffectsRenderingMode Enum
linktitle: Dml3DEffectsRenderingMode
articleTitle: Dml3DEffectsRenderingMode
second_title: Aspose.Words для .NET
description: Узнайте, как улучшить ваши документы с помощью перечисления Dml3DEffectsRenderingMode от Aspose.Words для превосходной визуализации трехмерных фигур и визуального эффекта.
type: docs
weight: 5650
url: /ru/net/aspose.words.saving/dml3deffectsrenderingmode/
---
## Dml3DEffectsRenderingMode enumeration

Указывает, как визуализируются эффекты 3D-форм.

```csharp
public enum Dml3DEffectsRenderingMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Basic | `0` | Легкий и стабильный рендеринг, основанный на внутреннем движке , но расширенные эффекты, такие как освещение, материалы и другие дополнительные эффекты , не отображаются при использовании этого режима. Подробности см. в документации. |
| Advanced | `1` | Рендеринг расширенного списка спецэффектов, включая расширенные 3D-эффекты , такие как скосы, освещение и материалы. |

## Примеры

Показывает, как визуализируются 3D-эффекты.

```csharp
Document doc = new Document(MyDir + "DrawingML shape 3D effects.docx");

RenderCallback warningCallback = new RenderCallback();
doc.WarningCallback = warningCallback;

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.Dml3DEffectsRenderingMode = Dml3DEffectsRenderingMode.Advanced;

doc.Save(ArtifactsDir + "PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf", saveOptions);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
