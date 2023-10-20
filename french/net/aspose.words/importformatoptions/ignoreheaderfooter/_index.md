---
title: ImportFormatOptions.IgnoreHeaderFooter
linktitle: IgnoreHeaderFooter
articleTitle: IgnoreHeaderFooter
second_title: Aspose.Words pour .NET
description: ImportFormatOptions IgnoreHeaderFooter propriété. Obtient ou définit une valeur booléenne qui spécifie que le formatage source du contenu des entêtes/pieds de page est ignoré siKeepSourceFormatting Le mode est utilisé. La valeur par défaut estvrai  en C#.
type: docs
weight: 40
url: /fr/net/aspose.words/importformatoptions/ignoreheaderfooter/
---
## ImportFormatOptions.IgnoreHeaderFooter property

Obtient ou définit une valeur booléenne qui spécifie que le formatage source du contenu des en-têtes/pieds de page est ignoré siKeepSourceFormatting Le mode est utilisé. La valeur par défaut est`vrai` .

```csharp
public bool IgnoreHeaderFooter { get; set; }
```

## Exemples

Montre comment spécifier d'ignorer ou non le formatage source du contenu des en-têtes/pieds de page.

```csharp
Document dstDoc = new Document(MyDir + "Document.docx");
Document srcDoc = new Document(MyDir + "Header and footer types.docx");

ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreHeaderFooter = false;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

### Voir également

* class [ImportFormatOptions](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
