---
title: "Méthode Aspose::Words::DocumentBase::ImportNode"
linktitle: "ImportNode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DocumentBase::ImportNode. Importe un nœud d'un autre document vers le document actuel en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words/documentbase/importnode/
---
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Importe un nœud d'un autre document vers le document actuel.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Le nœud à importer. |
| isImportChildren | bool | **true** pour importer tous les nœuds enfants de manière récursive ; sinon, **false**. |

### ReturnValue

Le nœud cloné qui appartient au document actuel.
## Remarques


Cette méthode utilise l'option [UseDestinationStyles](../../importformatmode/) pour résoudre le formatage.

L'importation d'un nœud crée une copie du nœud source appartenant au document d'importation. Le nœud retourné n'a pas de parent. Le nœud source n'est ni modifié ni supprimé du document original.

Avant qu'un nœud provenant d'un autre document puisse être inséré dans ce document, il doit être importé. Pendant l'importation, les propriétés spécifiques au document telles que les références aux styles et aux listes sont traduites de l'original vers le document d'importation. Après que le nœud a été importé, il peut être inséré à l'endroit approprié dans le document en utilisant [InsertBefore1()</see> ou <see cref="Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertAfter1()](../).

Si le nœud source appartient déjà au document de destination, alors un clone profond du nœud source est simplement créé.

## Exemples



Montre comment importer un nœud d'un document à un autre.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

srcDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(srcDoc, u"Source document first paragraph text."));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(dstDoc, u"Destination document first paragraph text."));

// Chaque nœud possède un document parent, qui est le document contenant le nœud.
// Insérer un nœud dans un document auquel le nœud n'appartient pas déclenchera une exception.
ASPOSE_ASSERT_NE(dstDoc, srcDoc->get_FirstSection()->get_Document());
ASSERT_THROW(static_cast<std::function<void()>>([&dstDoc, &srcDoc]() -> void
{
    dstDoc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(srcDoc->get_FirstSection());
})(), System::ArgumentException);

// Utilisez la méthode ImportNode pour créer une copie d'un nœud, qui aura le document
// qui a appelé la méthode ImportNode défini comme son nouveau document propriétaire.
auto importedSection = System::ExplicitCast<Aspose::Words::Section>(dstDoc->ImportNode(srcDoc->get_FirstSection(), true));

ASPOSE_ASSERT_EQ(dstDoc, importedSection->get_Document());

// Nous pouvons maintenant insérer le nœud dans le document.
dstDoc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(importedSection);

ASSERT_EQ(u"Destination document first paragraph text.\r\nSource document first paragraph text.\r\n", dstDoc->ToString(Aspose::Words::SaveFormat::Text));
```

## Voir aussi

* Class [Node](../../node/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) method


Importe un nœud d'un autre document vers le document actuel avec une option pour contrôler le formatage.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren, Aspose::Words::ImportFormatMode importFormatMode)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Le nœud à importer. |
| isImportChildren | bool | **true** pour importer tous les nœuds enfants de manière récursive ; sinon, **false**. |
| importFormatMode | Aspose::Words::ImportFormatMode | Spécifie comment fusionner le formatage de style qui entre en conflit. |

### ReturnValue

Le nœud cloné et importé. Le nœud appartient au document de destination, mais n'a pas de parent.
## Remarques


Cette surcharge est utile pour contrôler la façon dont les styles et le formatage des listes sont importés.

L'importation d'un nœud crée une copie du nœud source appartenant au document d'importation. Le nœud retourné n'a pas de parent. Le nœud source n'est ni modifié ni supprimé du document original.

Avant qu'un nœud provenant d'un autre document puisse être inséré dans ce document, il doit être importé. Pendant l'importation, les propriétés spécifiques au document telles que les références aux styles et aux listes sont traduites de l'original vers le document d'importation. Après que le nœud a été importé, il peut être inséré à l'endroit approprié dans le document en utilisant [InsertBefore1()</see> ou <see cref="Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertAfter1()](../).

Si le nœud source appartient déjà au document de destination, alors un clone profond du nœud source est simplement créé.

## Exemples



Montre comment importer un nœud du document source vers le document de destination avec des options spécifiques.
```cpp
// Créez deux documents et ajoutez un style de caractère à chaque document.
// Configurez les styles pour qu'ils aient le même nom, mais un formatage de texte différent.
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> srcStyle = srcDoc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"My style");
srcStyle->get_Font()->set_Name(u"Courier New");
auto srcBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);
srcBuilder->get_Font()->set_Style(srcStyle);
srcBuilder->Writeln(u"Source document text.");

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> dstStyle = dstDoc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"My style");
dstStyle->get_Font()->set_Name(u"Calibri");
auto dstBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
dstBuilder->get_Font()->set_Style(dstStyle);
dstBuilder->Writeln(u"Destination document text.");

// Importez la section du document de destination dans le document source, provoquant une collision de noms de style.
// Si nous utilisons les styles de destination, alors le texte source importé avec le même nom de style
// que le texte de destination adoptera le style de destination.
auto importedSection = System::ExplicitCast<Aspose::Words::Section>(dstDoc->ImportNode(srcDoc->get_FirstSection(), true, Aspose::Words::ImportFormatMode::UseDestinationStyles));
ASSERT_EQ(dstStyle->get_Font()->get_Name(), importedSection->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());
ASSERT_EQ(dstStyle->get_Name(), importedSection->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_StyleName());

// Si nous utilisons ImportFormatMode.KeepDifferentStyles, le style source est préservé,
// et le conflit de noms se résout en ajoutant un suffixe.
dstDoc->ImportNode(srcDoc->get_FirstSection(), true, Aspose::Words::ImportFormatMode::KeepDifferentStyles);
ASSERT_EQ(dstStyle->get_Font()->get_Name(), dstDoc->get_Styles()->idx_get(u"My style")->get_Font()->get_Name());
ASSERT_EQ(srcStyle->get_Font()->get_Name(), dstDoc->get_Styles()->idx_get(u"My style_0")->get_Font()->get_Name());
```

## Voir aussi

* Class [Node](../../node/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) method


Importe un nœud d'un autre document vers le document actuel avec une option pour contrôler le formatage.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Le nœud à importer. |
| isImportChildren | bool | **true** pour importer tous les nœuds enfants de manière récursive ; sinon, **false**. |
| importFormatMode | Aspose::Words::ImportFormatMode | Spécifie comment fusionner le formatage de style qui entre en conflit. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Permet de spécifier diverses options de formatage supplémentaires. |

### ReturnValue

Le nœud cloné et importé. Le nœud appartient au document de destination, mais n'a pas de parent.
## Remarques


Cette surcharge est utile pour contrôler la façon dont les styles et le formatage des listes sont importés.

L'importation d'un nœud crée une copie du nœud source appartenant au document d'importation. Le nœud retourné n'a pas de parent. Le nœud source n'est ni modifié ni supprimé du document original.

Avant qu'un nœud provenant d'un autre document puisse être inséré dans ce document, il doit être importé. Pendant l'importation, les propriétés spécifiques au document telles que les références aux styles et aux listes sont traduites de l'original vers le document d'importation. Après que le nœud a été importé, il peut être inséré à l'endroit approprié dans le document en utilisant [InsertBefore1()</see> ou <see cref="Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertAfter1()](../).

Si le nœud source appartient déjà au document de destination, alors un clone profond du nœud source est simplement créé.

## Exemples



Montre comment importer un nœud en résolvant les couleurs de thème source des formes.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

// Déplacez-vous vers le pied de page principal et insérez une forme qui utilise les couleurs du thème.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 50);
shape->get_Stroke()->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
// Importez le pied de page source dans le document de destination avec les couleurs du thème résolues,
// afin que la forme conserve sa couleur réelle du document source.
System::SharedPtr<Aspose::Words::HeaderFooter> footer = srcDoc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ResolveThemeColors(true);
auto importedFooter = System::ExplicitCast<Aspose::Words::HeaderFooter>(dstDoc->ImportNode(footer, true, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options));

dstDoc->get_FirstSection()->get_HeadersFooters()->Add(importedFooter);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBase.ImportNodeWithResolveThemeColors.docx");
```

## Voir aussi

* Class [Node](../../node/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
