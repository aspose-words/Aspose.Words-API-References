---
title: Font.NoProofing
linktitle: NoProofing
articleTitle: NoProofing
second_title: Aspose.Words для .NET
description: Font NoProofing свойство. Истинно если форматированные символы не подлежат проверке орфографии на С#.
type: docs
weight: 280
url: /ru/net/aspose.words/font/noproofing/
---
## Font.NoProofing property

Истинно, если форматированные символы не подлежат проверке орфографии.

```csharp
public bool NoProofing { get; set; }
```

## Примеры

Показывает, как предотвратить проверку орфографии текста в Microsoft Word.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Обычно Microsoft Word подчеркивает орфографические ошибки неровным красным подчеркиванием.
// Мы можем снять флаг «Без проверки», чтобы создать часть текста, которая
// обходит проверку орфографии, полностью отключая ее.
builder.Font.NoProofing = true;

builder.Writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc.Save(ArtifactsDir + "Font.NoProofing.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
