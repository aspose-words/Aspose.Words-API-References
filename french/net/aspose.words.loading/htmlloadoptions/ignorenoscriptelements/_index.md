---
title: HtmlLoadOptions.IgnoreNoscriptElements
linktitle: IgnoreNoscriptElements
articleTitle: IgnoreNoscriptElements
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété HtmlLoadOptions IgnoreNoscriptElements optimise votre analyse HTML en contrôlant les éléments noscript. Améliorez vos performances web dès aujourd'hui !
type: docs
weight: 40
url: /fr/net/aspose.words.loading/htmlloadoptions/ignorenoscriptelements/
---
## HtmlLoadOptions.IgnoreNoscriptElements property

Obtient ou définit une valeur indiquant s'il faut ignorer les éléments HTML &lt;noscript&gt;. La valeur par défaut est`FAUX` .

```csharp
public bool IgnoreNoscriptElements { get; set; }
```

## Remarques

Comme MS Word, Aspose.Words ne prend pas en charge les scripts et charge par défaut le contenu des éléments &lt;noscript&gt; dans le document résultant. Cependant, dans la plupart des navigateurs, les scripts sont pris en charge et le contenu de &lt;noscript&gt; n'est pas visible. Si vous définissez cette propriété sur`vrai` force Aspose.Words à ignorer tous les éléments &lt;noscript&gt; et aide à produire des documents qui ressemblent davantage à ce qui est vu dans les navigateurs.

## Exemples

Montre comment ignorer les éléments HTML &lt;noscript&gt;.

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

### Voir également

* class [HtmlLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
