---
title: HtmlSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words для .NET
description: Оптимизируйте свой веб-контент с помощью HtmlSaveOptions, чтобы легко удалить JavaScript из ссылок, повысить производительность и улучшить взаимодействие с пользователем.
type: docs
weight: 410
url: /ru/net/aspose.words.saving/htmlsaveoptions/removejavascriptfromlinks/
---
## HtmlSaveOptions.RemoveJavaScriptFromLinks property

Указывает, будет ли JavaScript удален из ссылок. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## Примечания

Если эта опция включена, все ссылки, содержащие JavaScript (например, ссылки с "javascript:" в атрибуте href) будут заменены на "javascript:void(0)". Это может помочь предотвратить потенциальные риски безопасности, такие как атаки XSS.

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
