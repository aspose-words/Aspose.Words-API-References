---
title: HtmlLoadOptions.IgnoreNoscriptElements
second_title: Справочник по API Aspose.Words для .NET
description: HtmlLoadOptions свойство. Получает или задает значение указывающее следует ли игнорировать HTMLэлементы noscript. Значение по умолчаниюЛОЖЬ .
type: docs
weight: 40
url: /ru/net/aspose.words.loading/htmlloadoptions/ignorenoscriptelements/
---
## HtmlLoadOptions.IgnoreNoscriptElements property

Получает или задает значение, указывающее, следует ли игнорировать HTML-элементы &lt;noscript&gt;. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool IgnoreNoscriptElements { get; set; }
```

### Примечания

Как и MS Word, Aspose.Words не поддерживает скрипты и по умолчанию загружает содержимое &lt;noscript&gt; elements в результирующий документ. Однако в большинстве браузеров сценарии поддерживаются, и содержимое &lt;noscript&gt; не отображается. Установка этого свойства в`истинный` заставляет Aspose.Words игнорировать все элементы &lt;noscript&gt; и помогает создавать документы, которые выглядят ближе к тому, что отображается в браузерах.

### Примеры

Показывает, как игнорировать HTML-элементы &lt;noscript&gt;.

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
* пространство имен [Aspose.Words.Loading](../../htmlloadoptions/)
* сборка [Aspose.Words](../../../)


