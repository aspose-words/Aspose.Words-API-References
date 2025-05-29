---
title: ReplacerContext.SetReplacement
linktitle: SetReplacement
articleTitle: SetReplacement
second_title: Aspose.Words для .NET
description: Улучшите операции поиска и замены с помощью метода ReplacerContext SetReplacement, обеспечивающего бесшовное управление шаблонами и заменой для повышения эффективности.
type: docs
weight: 30
url: /ru/net/aspose.words.lowcode/replacercontext/setreplacement/
---
## SetReplacement(*string, string*) {#setreplacement}

Устанавливает шаблон и замену, используемые операцией поиска/замены.

```csharp
public void SetReplacement(string pattern, string replacement)
```

## Примечания

Использование этого метода отменяет ранее установленный шаблон и замену.

## Примеры

Показывает, как заменить строку в документе, используя контекст.

```csharp
// Существует несколько способов заменить строку в документе:
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

ReplacerContext replacerContext = new ReplacerContext();
replacerContext.SetReplacement(pattern, replacement);
replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

Replacer.Create(replacerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.ReplaceContext.docx")
    .Execute();
```

Показывает, как заменить строку в документе, используя документы из потока с использованием контекста.

```csharp
// Существует несколько способов заменить строку в документе, используя документы из потока:
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

using (FileStream streamIn = new FileStream(MyDir + "Footer.docx", FileMode.Open, FileAccess.Read))
{
    ReplacerContext replacerContext = new ReplacerContext();
    replacerContext.SetReplacement(pattern, replacement);
    replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceContextStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Create(replacerContext)
        .From(streamIn)
        .To(streamOut, SaveFormat.Docx)
        .Execute();
}
```

### Смотрите также

* class [ReplacerContext](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## SetReplacement(*Regex, string*) {#setreplacement_1}

Устанавливает шаблон и замену, используемые операцией поиска/замены.

```csharp
public void SetReplacement(Regex pattern, string replacement)
```

## Примечания

Использование этого метода отменяет ранее установленный шаблон и замену.

## Примеры

Показывает, как заменить строку регулярным выражением в документе, используя контекст.

```csharp
// Существует несколько способов заменить строку регулярным выражением в документе:
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

ReplacerContext replacerContext = new ReplacerContext();
replacerContext.SetReplacement(pattern, replacement);
replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

Replacer.Create(replacerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.ReplaceContextRegex.docx")
    .Execute();
```

Показывает, как заменить строку регулярным выражением в документе, используя документы из потока с использованием контекста.

```csharp
// Существует несколько способов заменить строку регулярным выражением в документе, используя документы из потока:
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

using (FileStream streamIn = new FileStream(MyDir + "Replace regex.docx", FileMode.Open, FileAccess.Read))
{
    ReplacerContext replacerContext = new ReplacerContext();
    replacerContext.SetReplacement(pattern, replacement);
    replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceContextStreamRegex.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Create(replacerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Смотрите также

* class [ReplacerContext](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
