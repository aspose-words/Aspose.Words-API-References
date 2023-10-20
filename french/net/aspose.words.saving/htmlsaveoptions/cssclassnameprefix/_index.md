---
title: HtmlSaveOptions.CssClassNamePrefix
linktitle: CssClassNamePrefix
articleTitle: CssClassNamePrefix
second_title: Aspose.Words pour .NET
description: HtmlSaveOptions CssClassNamePrefix propriété. Spécifie un préfixe qui est ajouté à tous les noms de classe CSS. La valeur par défaut est une chaîne vide et les noms de classe CSS générés nont pas de préfixe commun en C#.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/htmlsaveoptions/cssclassnameprefix/
---
## HtmlSaveOptions.CssClassNamePrefix property

Spécifie un préfixe qui est ajouté à tous les noms de classe CSS. La valeur par défaut est une chaîne vide et les noms de classe CSS générés n'ont pas de préfixe commun.

```csharp
public string CssClassNamePrefix { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentException | La valeur n'est pas vide et n'est pas un identifiant CSS valide. |

## Remarques

Si cette valeur n'est pas vide, toutes les classes CSS générées par Aspose.Words commenceront par le préfixe spécifié. Cela peut être utile, par exemple, si vous ajoutez du CSS personnalisé aux documents générés et que vous souhaitez éviter les conflits de noms class .

Si la valeur n'est pas`nul` ou vide, il doit s'agir d'un identifiant CSS valide.

## Exemples

Montre comment enregistrer un document au format HTML et ajouter un préfixe à tous ses noms de classe CSS.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

HtmlSaveOptions saveOptions = new HtmlSaveOptions
{
    CssStyleSheetType = CssStyleSheetType.External,
    CssClassNamePrefix = "myprefix-"
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.html");

Assert.True(outDocContents.Contains("<p class=\"myprefix-Header\">"));
Assert.True(outDocContents.Contains("<p class=\"myprefix-Footer\">"));

outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.css");

Assert.True(outDocContents.Contains(".myprefix-Footer { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt }\r\n" +
                                    ".myprefix-Header { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt }\r\n"));
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
