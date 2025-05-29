---
title: SvgSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words для .NET
description: Оптимизируйте файлы SVG с помощью SvgSaveOptions, легко удаляйте JavaScript из ссылок для более чистого кода. Повысьте производительность и безопасность с помощью этой простой настройки!
type: docs
weight: 60
url: /ru/net/aspose.words.saving/svgsaveoptions/removejavascriptfromlinks/
---
## SvgSaveOptions.RemoveJavaScriptFromLinks property

Указывает, будет ли JavaScript удален из ссылок. Значение по умолчанию:`ЛОЖЬ` . Если эта опция включена, все ссылки, содержащие JavaScript, будут заменены на «javascript:void(0)».

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## Примеры

Показывает, как удалить JavaScript из ссылок (svg).

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "SvgSaveOptions.RemoveJavaScriptFromLinksSvg.html", saveOptions);
```

### Смотрите также

* class [SvgSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
