---
title: ImportFormatOptions.IgnoreHeaderFooter
second_title: Référence de l'API Aspose.Words pour .NET
description: ImportFormatOptions propriété. Obtient ou définit une valeur booléenne qui spécifie que la mise en forme source du contenu des entêtes/pieds de page est ignorée siKeepSourceFormatting mode est utilisé. La valeur par défaut estvrai .
type: docs
weight: 30
url: /fr/net/aspose.words/importformatoptions/ignoreheaderfooter/
---
## ImportFormatOptions.IgnoreHeaderFooter property

Obtient ou définit une valeur booléenne qui spécifie que la mise en forme source du contenu des en-têtes/pieds de page est ignorée siKeepSourceFormatting mode est utilisé. La valeur par défaut est`vrai` .

```csharp
public bool IgnoreHeaderFooter { get; set; }
```

### Exemples

Montre comment spécifier d'ignorer ou non la mise en forme source du contenu des en-têtes/pieds de page.

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
* espace de noms [Aspose.Words](../../importformatoptions/)
* Assemblée [Aspose.Words](../../../)


