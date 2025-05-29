---
title: XamlFlowSaveOptions.ReplaceBackslashWithYenSign
linktitle: ReplaceBackslashWithYenSign
articleTitle: ReplaceBackslashWithYenSign
second_title: Aspose.Words для .NET
description: Узнайте, как свойство ReplaceBackslashWithYenSign класса XamlFlowSaveOptions улучшает форматирование данных, преобразуя обратные косые черты в знаки иены. Значение по умолчанию — false.
type: docs
weight: 50
url: /ru/net/aspose.words.saving/xamlflowsaveoptions/replacebackslashwithyensign/
---
## XamlFlowSaveOptions.ReplaceBackslashWithYenSign property

Указывает, следует ли заменять символы обратной косой черты на знаки йены. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ReplaceBackslashWithYenSign { get; set; }
```

## Примечания

По умолчанию Aspose.Words имитирует поведение MS Word и не заменяет символы обратной косой черты на знаки йены в сгенерированных документах XAML. Однако предыдущие версии Aspose.Words выполняли такие замены в определенных сценариях. Этот флаг обеспечивает обратную совместимость с предыдущими версиями Aspose.Words.

## Примеры

Показывает, как заменить символы обратной косой черты на знаки йены (XAML).

```csharp
Document doc = new Document(MyDir + "Korean backslash symbol.docx");

// По умолчанию Aspose.Words имитирует поведение MS Word и не заменяет символы обратной косой черты на знаки йены в
// сгенерированные HTML-документы. Однако предыдущие версии Aspose.Words выполняли такие замены в определенных
// сценарии. Этот флаг обеспечивает обратную совместимость с предыдущими версиями Aspose.Words.
XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions();
saveOptions.ReplaceBackslashWithYenSign = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.ReplaceBackslashWithYenSign.xaml", saveOptions);
```

### Смотрите также

* class [XamlFlowSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
