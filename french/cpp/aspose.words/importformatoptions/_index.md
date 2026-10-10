---
title: "classe Aspose::Words::ImportFormatOptions"
linktitle: "ImportFormatOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "classe Aspose::Words::ImportFormatOptions. Permet de spécifier diverses options d'importation pour formater la sortie. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 35000
url: /fr/cpp/aspose.words/importformatoptions/
---
## ImportFormatOptions class


Permet de spécifier diverses options d'importation pour formater la sortie. Pour en savoir plus, consultez l'article de documentation [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class ImportFormatOptions : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_AdjustSentenceAndWordSpacing](./get_adjustsentenceandwordspacing/)() const | Obtient ou définit une valeur booléenne qui indique s'il faut ajuster automatiquement l'espacement des phrases et des mots. La valeur par défaut est **false**. |
| [get_AppendDocumentWithNewPage](./get_appenddocumentwithnewpage/)() const | Obtient ou définit une valeur booléenne indiquant s'il faut changer le type de la première section importée en [NewPage](../sectionstart/) de manière forcée lors de l'appel de [AppendDocument()](../). La valeur par défaut est **true**. |
| [get_ForceCopyStyles](./get_forcecopystyles/)() const | Obtient ou définit une valeur booléenne indiquant s'il faut copier les styles conflictuels en mode [KeepSourceFormatting](../importformatmode/). La valeur par défaut est **false**. |
| [get_IgnoreHeaderFooter](./get_ignoreheaderfooter/)() const | Obtient ou définit une valeur booléenne qui indique que le formatage source du contenu des en-têtes/pieds de page est ignoré si le mode [KeepSourceFormatting](../importformatmode/) est utilisé. La valeur par défaut est **true**. |
| [get_IgnoreTextBoxes](./get_ignoretextboxes/)() const | Obtient ou définit une valeur booléenne qui indique que le formatage source du contenu des zones de texte est ignoré si le mode [KeepSourceFormatting](../importformatmode/) est utilisé. La valeur par défaut est **true**. |
| [get_KeepSourceNumbering](./get_keepsourcenumbering/)() const | Obtient ou définit une valeur booléenne qui indique comment la numérotation sera importée lorsqu'elle entre en conflit dans les documents source et destination. La valeur par défaut est **false**. |
| [get_MergePastedLists](./get_mergepastedlists/)() const | Obtient ou définit une valeur booléenne qui indique si les listes collées seront fusionnées avec les listes environnantes. La valeur par défaut est **false**. |
| [get_ResolveThemeColors](./get_resolvethemecolors/)() const | Obtient ou définit une valeur booléenne qui indique s'il faut résoudre de manière forcée les couleurs de thème des formes. La valeur par défaut est **false**. |
| [get_SmartStyleBehavior](./get_smartstylebehavior/)() const | Obtient ou définit une valeur booléenne qui indique comment les styles seront importés lorsqu'ils portent le même nom dans les documents source et destination. La valeur par défaut est **false**. |
| [GetType](./gettype/)() const override |  |
| [ImportFormatOptions](./importformatoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AdjustSentenceAndWordSpacing](./set_adjustsentenceandwordspacing/)(bool) | Définisseur pour [Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing](./get_adjustsentenceandwordspacing/). |
| [set_AppendDocumentWithNewPage](./set_appenddocumentwithnewpage/)(bool) | Définisseur pour [Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage](./get_appenddocumentwithnewpage/). |
| [set_ForceCopyStyles](./set_forcecopystyles/)(bool) | Définisseur pour [Aspose::Words::ImportFormatOptions::get_ForceCopyStyles](./get_forcecopystyles/). |
| [set_IgnoreHeaderFooter](./set_ignoreheaderfooter/)(bool) | Définisseur pour [Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter](./get_ignoreheaderfooter/). |
| [set_IgnoreTextBoxes](./set_ignoretextboxes/)(bool) | Définisseur pour [Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes](./get_ignoretextboxes/). |
| [set_KeepSourceNumbering](./set_keepsourcenumbering/)(bool) | Définisseur pour [Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering](./get_keepsourcenumbering/). |
| [set_MergePastedLists](./set_mergepastedlists/)(bool) | Définisseur pour [Aspose::Words::ImportFormatOptions::get_MergePastedLists](./get_mergepastedlists/). |
| [set_ResolveThemeColors](./set_resolvethemecolors/)(bool) | Définisseur pour [Aspose::Words::ImportFormatOptions::get_ResolveThemeColors](./get_resolvethemecolors/). |
| [set_SmartStyleBehavior](./set_smartstylebehavior/)(bool) | Définisseur pour [Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior](./get_smartstylebehavior/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
