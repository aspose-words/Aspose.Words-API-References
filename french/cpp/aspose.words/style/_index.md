---
title: "classe Aspose::Words::Style"
linktitle: "Style"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Style. Représente un style intégré ou défini par l'utilisateur. Pour en savoir plus, consultez l’article de documentation en C++."
type: docs
weight: 64000
url: /fr/cpp/aspose.words/style/
---
## Style class


Représente un style intégré ou défini par l'utilisateur. Pour en savoir plus, consultez l'article de documentation [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/).

```cpp
class Style : public Aspose::Words::IParaAttrSource,
              public Aspose::Words::IRunAttrSource
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Compare avec le style spécifié. Les Istds de styles sont comparés uniquement pour les styles intégrés. Les valeurs par défaut des styles ne sont pas incluses dans la comparaison. Le style de base, le style lié et le style du paragraphe suivant sont comparés de manière récursive. |
| [get_Aliases](./get_aliases/)() | Obtient tous les alias de ce style. Si le style n’a aucun alias, un tableau vide de chaînes est retourné. |
| [get_AutomaticallyUpdate](./get_automaticallyupdate/)() const | Spécifie si ce style est automatiquement redéfini en fonction de la valeur appropriée. |
| [get_BaseStyleName](./get_basestylename/)() | Obtient/definit le nom du style sur lequel ce style est basé. |
| [get_BuiltIn](./get_builtin/)() | Vrai si ce style fait partie des styles intégrés dans MS Word. |
| [get_Document](./get_document/)() | Obtient le document propriétaire. |
| [get_Font](./get_font/)() | Obtient le formatage de caractères du style. |
| [get_IsHeading](./get_isheading/)() | Vrai lorsque le style fait partie des styles de titre intégrés. |
| [get_IsQuickStyle](./get_isquickstyle/)() const | Spécifie si ce style est affiché dans la galerie rapide [Style](./) de l’interface MS Word. |
| [get_LinkedStyleName](./get_linkedstylename/)() | Obtient/definit le nom du [Style](./) lié à celui-ci. Retourne une chaîne vide si aucun style n’est lié. |
| [get_List](./get_list/)() | Obtient la liste qui définit le formatage de ce style de liste. |
| [get_ListFormat](./get_listformat/)() | Fournit l’accès aux propriétés de formatage de liste d’un style de paragraphe. |
| [get_Locked](./get_locked/)() const | Spécifie si ce style est verrouillé. |
| [get_Name](./get_name/)() const | Obtient ou définit le nom du style. |
| [get_NextParagraphStyleName](./get_nextparagraphstylename/)() | Obtient/definit le nom du style à appliquer automatiquement à un nouveau paragraphe inséré après un paragraphe formaté avec le style spécifié. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Obtient le formatage du paragraphe du style. |
| [get_Priority](./get_priority/)() const | Obtient/definit la valeur entière qui représente la priorité de tri des styles dans le volet des tâches Styles. |
| [get_SemiHidden](./get_semihidden/)() const | Obtient/definit si le style est masqué dans la galerie des Styles et dans le volet des Styles. |
| [get_StyleIdentifier](./get_styleidentifier/)() const | Obtient l'identifiant de style indépendant de la locale pour un style intégré. |
| [get_Styles](./get_styles/)() const | Obtient la collection de styles à laquelle ce style appartient. |
| [get_Type](./get_type/)() const | Obtient le type de style (paragraphe ou caractère). |
| [get_UnhideWhenUsed](./get_unhidewhenused/)() const | Obtient/definit si le style utilisé dans le document actuel se dévoile dans la galerie des Styles et dans le volet des Styles. Vrai lorsque le style utilisé doit être affiché dans la galerie des Styles. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Supprime le style spécifié du document. |
| [set_AutomaticallyUpdate](./set_automaticallyupdate/)(bool) | Définisseur pour [Aspose::Words::Style::get_AutomaticallyUpdate](./get_automaticallyupdate/). |
| [set_BaseStyleName](./set_basestylename/)(const System::String\&) | Définisseur pour [Aspose::Words::Style::get_BaseStyleName](./get_basestylename/). |
| [set_IsQuickStyle](./set_isquickstyle/)(bool) | Définisseur pour [Aspose::Words::Style::get_IsQuickStyle](./get_isquickstyle/). |
| [set_LinkedStyleName](./set_linkedstylename/)(const System::String\&) | Définisseur pour [Aspose::Words::Style::get_LinkedStyleName](./get_linkedstylename/). |
| [set_Locked](./set_locked/)(bool) | Définisseur pour [Aspose::Words::Style::get_Locked](./get_locked/). |
| [set_Name](./set_name/)(const System::String\&) | Définisseur pour [Aspose::Words::Style::get_Name](./get_name/). |
| [set_NextParagraphStyleName](./set_nextparagraphstylename/)(const System::String\&) | Définisseur pour [Aspose::Words::Style::get_NextParagraphStyleName](./get_nextparagraphstylename/). |
| [set_Priority](./set_priority/)(int32_t) | Définisseur pour [Aspose::Words::Style::get_Priority](./get_priority/). |
| [set_SemiHidden](./set_semihidden/)(bool) | Définisseur pour [Aspose::Words::Style::get_SemiHidden](./get_semihidden/). |
| [set_UnhideWhenUsed](./set_unhidewhenused/)(bool) | Définisseur pour [Aspose::Words::Style::get_UnhideWhenUsed](./get_unhidewhenused/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment créer et appliquer un style personnalisé.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Size(16);
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
// Redéfinir automatiquement le style.
style->set_AutomaticallyUpdate(true);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Applique l'un des styles du document au paragraphe que le constructeur de document est en train de créer.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Style> firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

ASPOSE_ASSERT_EQ(style, firstParagraphStyle);

// Supprime notre style personnalisé de la collection de styles du document.
doc->get_Styles()->idx_get(u"MyStyle")->Remove();

firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

// Tout texte qui utilisait un style supprimé revient au formatage par défaut.
ASSERT_FALSE(doc->get_Styles()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Style>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Style> s)>>([](System::SharedPtr<Aspose::Words::Style> s) -> bool
{
    return s->get_Name() == u"MyStyle";
}))));
ASSERT_EQ(u"Times New Roman", firstParagraphStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(12.0, firstParagraphStyle->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), firstParagraphStyle->get_Font()->get_Color().ToArgb());
```


Montre comment créer et utiliser un style de paragraphe avec un formatage de liste.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez un style de paragraphe personnalisé.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Créez une liste et assurez-vous que les paragraphes qui utilisent ce style utiliseront cette liste.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Appliquez le style de paragraphe au paragraphe actuel du constructeur de document, puis ajoutez du texte.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Modifiez le style du DocumentBuilder pour qu'il n'ait aucun format de liste et écrivez un autre paragraphe.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
