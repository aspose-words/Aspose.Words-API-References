---
title: HtmlSaveOptions.ReplaceBackslashWithYenSign
linktitle: ReplaceBackslashWithYenSign
articleTitle: ReplaceBackslashWithYenSign
second_title: Aspose.Words для .NET
description: Узнайте, как свойство HtmlSaveOptions ReplaceBackslashWithYenSign улучшает ваш HTML-вывод, преобразуя обратные косые черты в знаки йены. По умолчанию — false.
type: docs
weight: 420
url: /ru/net/aspose.words.saving/htmlsaveoptions/replacebackslashwithyensign/
---
## HtmlSaveOptions.ReplaceBackslashWithYenSign property

Указывает, следует ли заменять символы обратной косой черты на знаки йены. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ReplaceBackslashWithYenSign { get; set; }
```

## Примечания

По умолчанию Aspose.Words имитирует поведение MS Word и не заменяет символы обратной косой черты на знаки йены в сгенерированных HTML-документах. Однако предыдущие версии Aspose.Words выполняли такие замены в определенных сценариях. Этот флаг обеспечивает обратную совместимость с предыдущими версиями Aspose.Words.

## Примеры

Показывает, как заменить символы обратной косой черты на знаки йены (Html).

```csharp
Document doc = new Document(MyDir + "Korean backslash symbol.docx");

// По умолчанию Aspose.Words имитирует поведение MS Word и не заменяет символы обратной косой черты на знаки йены в
// сгенерированные HTML-документы. Однако предыдущие версии Aspose.Words выполняли такие замены в определенных
// сценарии. Этот флаг обеспечивает обратную совместимость с предыдущими версиями Aspose.Words.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ReplaceBackslashWithYenSign = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.ReplaceBackslashWithYenSign.html", saveOptions);
```

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
