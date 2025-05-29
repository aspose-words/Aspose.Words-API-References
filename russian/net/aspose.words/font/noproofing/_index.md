---
title: Font.NoProofing
linktitle: NoProofing
articleTitle: NoProofing
second_title: Aspose.Words для .NET
description: Откройте для себя Font NoProofing. Предотвратите проверку орфографии в отформатированном тексте для более чистого дизайна. Улучшите свои документы точностью и профессионализмом!
type: docs
weight: 280
url: /ru/net/aspose.words/font/noproofing/
---
## Font.NoProofing property

Истинно, когда отформатированные символы не подлежат проверке орфографии.

```csharp
public bool NoProofing { get; set; }
```

## Примеры

Показывает, как запретить проверку орфографии текста в Microsoft Word.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Обычно Microsoft Word подчеркивает орфографические ошибки неровной красной линией.
// Мы можем снять флаг «NoProofing», чтобы создать часть текста, которая
// обходит проверку орфографии, полностью отключая ее.
builder.Font.NoProofing = true;

builder.Writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc.Save(ArtifactsDir + "Font.NoProofing.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
