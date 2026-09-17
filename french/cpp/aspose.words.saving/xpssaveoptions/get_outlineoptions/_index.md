---
title: "Aspose::Words::Saving::XpsSaveOptions::get_OutlineOptions méthode"
linktitle: "get_OutlineOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::XpsSaveOptions::get_OutlineOptions méthode. Permet de spécifier les options de contour en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.saving/xpssaveoptions/get_outlineoptions/
---
## XpsSaveOptions::get_OutlineOptions method


Permet de spécifier les options de contour.

```cpp
System::SharedPtr<Aspose::Words::Saving::OutlineOptions> Aspose::Words::Saving::XpsSaveOptions::get_OutlineOptions() const
```

## Remarques


Notez que l'option [ExpandedOutlineLevels](../../outlineoptions/get_expandedoutlinelevels/) ne fonctionnera pas lors de l'enregistrement au format XPS.

## Exemples



Montre comment limiter le niveau des titres qui apparaîtront dans le plan d'un document XPS enregistré.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez des titres pouvant servir d'entrées de table des matières aux niveaux 1, 2, puis 3.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsHeading());

builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);

builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);

builder->Writeln(u"Heading 1.2.1");
builder->Writeln(u"Heading 1.2.2");

// Créez un objet "XpsSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .XPS.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Xps, saveOptions->get_SaveFormat());

// Le document XPS de sortie contiendra un plan, une table des matières qui répertorie les titres dans le corps du document.
// Cliquer sur une entrée de ce plan nous amènera à l'emplacement du titre correspondant.
// Définissez la propriété "HeadingsOutlineLevels" sur "2" pour exclure tous les titres dont le niveau est supérieur à 2 du plan.
// Les deux derniers titres que nous avons insérés ci-dessus n'apparaîtront pas.
saveOptions->get_OutlineOptions()->set_HeadingsOutlineLevels(2);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

## Voir aussi

* Class [OutlineOptions](../../outlineoptions/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
