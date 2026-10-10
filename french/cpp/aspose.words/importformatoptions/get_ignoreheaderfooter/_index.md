---
title: "Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter méthode"
linktitle: "get_IgnoreHeaderFooter"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter méthode. Obtient ou définit une valeur booléenne qui indique que le formatage source du contenu des en-têtes/pieds de page est ignoré si le mode KeepSourceFormatting est utilisé. La valeur par défaut est true en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words/importformatoptions/get_ignoreheaderfooter/
---
## ImportFormatOptions::get_IgnoreHeaderFooter method


Obtient ou définit une valeur booléenne qui indique que le formatage source du contenu des en-têtes/pieds de page est ignoré si le mode [KeepSourceFormatting](../../importformatmode/) est utilisé. La valeur par défaut est **true**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter() const
```


## Exemples



Montre comment spécifier l'ignorance ou non du formatage source du contenu des en-têtes/pieds de page.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Si 'IgnoreHeaderFooter' est false alors le formatage original du contenu de l'en-tête/pied de page
// Le fichier "Header and footer types.docx" sera utilisé.
// Si 'IgnoreHeaderFooter' est vrai, alors le formatage du contenu d'en-tête/pied de page
// Le fichier "Document.docx" sera utilisé.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_IgnoreHeaderFooter(false);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, importFormatOptions);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

## Voir aussi

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
