---
title: HtmlLoadOptions.IgnoreNoscriptElements
linktitle: IgnoreNoscriptElements
articleTitle: IgnoreNoscriptElements
second_title: Aspose.Words для .NET
description: HtmlLoadOptions IgnoreNoscriptElements свойство. Получает или задает значение указывающее следует ли игнорировать HTMLэлементы noscript. Значение по умолчаниюЛОЖЬ  на С#.
type: docs
weight: 40
url: /ru/net/aspose.words.loading/htmlloadoptions/ignorenoscriptelements/
---
## HtmlLoadOptions.IgnoreNoscriptElements property

Получает или задает значение, указывающее, следует ли игнорировать HTML-элементы &lt;noscript&gt;. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool IgnoreNoscriptElements { get; set; }
```

## Примечания

Как и MS Word, Aspose.Words не поддерживает скрипты и по умолчанию загружает содержимое &lt;noscript&gt; elements в результирующий документ. Однако в большинстве браузеров поддерживаются сценарии, и содержимое &lt;noscript&gt; не отображается. Установка этого свойства в`истинный` заставляет Aspose.Words игнорировать все элементы &lt;noscript&gt; elements и помогает создавать документы, которые выглядят ближе к тому, что видно в браузерах.

## Примеры

Показывает, как игнорировать элементы HTML &lt;noscript&gt;.

```csharp
const string html = @"
    <html>
      <head>
        <title>NOSCRIPT</title>
          <meta http-equiv=""Content-Type"" content=""text/html; charset=utf-8"">
          <script type=""text/javascript"">
            alert(""Hello, world!"");
          </script>
      </head>
    <body>
      <noscript><p>Your browser does not support JavaScript!</p></noscript>
    </body>
    </html>";

HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions();
htmlLoadOptions.IgnoreNoscriptElements = ignoreNoscriptElements;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), htmlLoadOptions);
doc.Save(ArtifactsDir + "HtmlLoadOptions.IgnoreNoscriptElements.pdf");
```

### Смотрите также

* class [HtmlLoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
