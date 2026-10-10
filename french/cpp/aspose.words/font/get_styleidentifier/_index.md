---
title: "Méthode Aspose::Words::Font::get_StyleIdentifier"
linktitle: "get_StyleIdentifier"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Font::get_StyleIdentifier méthode. Obtient ou définit l'identifiant de style indépendant de la locale du style de caractère appliqué à ce formatage en C++."
type: docs
weight: 43000
url: /fr/cpp/aspose.words/font/get_styleidentifier/
---
## Font::get_StyleIdentifier method


Obtient ou définit l'identifiant de style indépendant de la locale du style de caractère appliqué à ce formatage.

```cpp
Aspose::Words::StyleIdentifier Aspose::Words::Font::get_StyleIdentifier()
```


## Exemples



Montre comment modifier le style du texte existant.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ci-dessous, deux façons de référencer les styles.
// 1 -  Utilisation du nom du style:
builder->get_Font()->set_StyleName(u"Emphasis");
builder->Writeln(u"Text originally in \"Emphasis\" style");

// 2 -  Utilisation d'un identifiant de style intégré :
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::IntenseEmphasis);
builder->Writeln(u"Text originally in \"Intense Emphasis\" style");

// Convertir toutes les utilisations d'un style en un autre,
// en utilisant les méthodes ci‑dessus pour référencer les anciens et les nouveaux styles.
for (auto&& run : System::IterateOver<Aspose::Words::Run>(doc->GetChildNodes(Aspose::Words::NodeType::Run, true)))
{
    if (run->get_Font()->get_StyleName() == u"Emphasis")
    {
        run->get_Font()->set_StyleName(u"Strong");
    }

    if (run->get_Font()->get_StyleIdentifier() == Aspose::Words::StyleIdentifier::IntenseEmphasis)
    {
        run->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Strong);
    }
}

doc->Save(get_ArtifactsDir() + u"Font.ChangeStyle.docx");
```

## Voir aussi

* Enum [StyleIdentifier](../../styleidentifier/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
