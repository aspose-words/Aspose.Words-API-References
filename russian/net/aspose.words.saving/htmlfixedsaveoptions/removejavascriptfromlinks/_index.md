---
title: HtmlFixedSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words для .NET
description: Оптимизируйте свой HTML с помощью функции HtmlFixedSaveOptions RemoveJavaScriptFromLinks. Повысьте безопасность, удалив JavaScript из ссылок без усилий.
type: docs
weight: 140
url: /ru/net/aspose.words.saving/htmlfixedsaveoptions/removejavascriptfromlinks/
---
## HtmlFixedSaveOptions.RemoveJavaScriptFromLinks property

Указывает, будет ли JavaScript удален из ссылок. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## Примечания

Если эта опция включена, все ссылки, содержащие JavaScript (например, ссылки с "javascript:" в атрибуте href) будут заменены на "javascript:void(0)". Это может помочь предотвратить потенциальные риски безопасности, такие как атаки XSS.

## Примеры

Показывает, как удалить JavaScript из ссылок.

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

Показывает, как удалить JavaScript из ссылок для фиксированных HTML-документов.

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

### Смотрите также

* class [HtmlFixedSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
