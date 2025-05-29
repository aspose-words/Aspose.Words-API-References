---
title: Style.Locked
linktitle: Locked
articleTitle: Locked
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Style Locked, управляйте блокировкой стилей для повышения гибкости дизайна и согласованности в ваших проектах. Раскройте свой творческий потенциал сегодня!
type: docs
weight: 120
url: /ru/net/aspose.words/style/locked/
---
## Style.Locked property

Указывает, заблокирован ли этот стиль.

```csharp
public bool Locked { get; set; }
```

## Примеры

Показывает, как заблокировать стиль.

```csharp
Document doc = new Document();

Style styleHeading1 = doc.Styles[StyleIdentifier.Heading1];
if (!styleHeading1.Locked)
    styleHeading1.Locked = true;

doc.Save(ArtifactsDir + "Styles.LockStyle.docx");
```

### Смотрите также

* class [Style](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
