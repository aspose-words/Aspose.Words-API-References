---
title: "Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior méthode"
linktitle: "get_SmartStyleBehavior"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior méthode. Obtient ou définit une valeur booléenne qui indique comment les styles seront importés lorsqu'ils ont des noms identiques dans les documents source et destination. La valeur par défaut est false en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words/importformatoptions/get_smartstylebehavior/
---
## ImportFormatOptions::get_SmartStyleBehavior method


Obtient ou définit une valeur booléenne qui indique comment les styles seront importés lorsqu'ils portent le même nom dans les documents source et destination. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior() const
```

## Remarques


Lorsque cette option est **activée**, le style source sera développé en attributs directs à l'intérieur d'un document de destination, si le mode d'importation [KeepSourceFormatting](../../importformatmode/) est utilisé.

Lorsque cette option est **désactivée**, le style source ne sera développé que s'il est numéroté. Les attributs de destination existants ne seront pas remplacés, y compris les listes.

## Exemples



Montre comment résoudre les styles en double lors de l'insertion de documents.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);

System::SharedPtr<Aspose::Words::Style> myStyle = builder->get_Document()->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
myStyle->get_Font()->set_Size(14);
myStyle->get_Font()->set_Name(u"Courier New");
myStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

builder->get_ParagraphFormat()->set_StyleName(myStyle->get_Name());
builder->Writeln(u"Hello world!");

// Clonez le document et modifiez le style "MyStyle" du clone, afin qu'il ait une couleur différente de celle de l'original.
// Si nous insérons le clone dans le document original, les deux styles portant le même nom provoqueront un conflit.
System::SharedPtr<Aspose::Words::Document> srcDoc = dstDoc->Clone();
srcDoc->get_Styles()->idx_get(u"MyStyle")->get_Font()->set_Color(System::Drawing::Color::get_Red());

// Lorsque nous activons SmartStyleBehavior et utilisons le mode d'importation KeepSourceFormatting,
// Aspose.Words résoudra les conflits de styles en convertissant les styles du document source.
// avec les mêmes noms que les styles de destination en attributs de paragraphe directs.
auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_SmartStyleBehavior(true);

builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.SmartStyleBehavior.docx");
```

## Voir aussi

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
