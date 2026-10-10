---
title: "Aspose::Words::DocumentBuilder class"
linktitle: "DocumentBuilder"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder class. Fournit des méthodes pour insérer du texte, des images et d'autres contenus, spécifier la police, le format des paragraphes et des sections. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 22000
url: /fr/cpp/aspose.words/documentbuilder/
---
## DocumentBuilder class


Fournit des méthodes pour insérer du texte, des images et d'autres contenus, spécifier la police, le format des paragraphes et des sections. Pour en savoir plus, consultez l'article de documentation [Document Builder Overview](https://docs.aspose.com/words/cpp/document-builder-overview/).

```cpp
class DocumentBuilder : public Aspose::Words::IRunAttrSource,
                        public Aspose::Words::IParaAttrSource,
                        public Aspose::Words::IRowAttrSource,
                        public Aspose::Words::ICellAttrSource
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [DeleteRow](./deleterow/)(int32_t, int32_t) | Supprime une ligne d'un tableau. |
| [DocumentBuilder](./documentbuilder/)() | Initialise une nouvelle instance de cette classe. |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) | Initialise une nouvelle instance de cette classe. |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Initialise une nouvelle instance de cette classe. |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) | Initialise une nouvelle instance de cette classe. |
| [EndBookmark](./endbookmark/)(const System::String\&) | Marque la position actuelle dans le document comme la fin d'un signet. |
| [EndColumnBookmark](./endcolumnbookmark/)(const System::String\&) | Marque la position actuelle dans le document comme la fin d'un signet de colonne. La position doit être dans une cellule de tableau. |
| [EndEditableRange](./endeditablerange/)() | Marque la position actuelle dans le document comme la fin d'une plage modifiable. |
| [EndEditableRange](./endeditablerange/)(const System::SharedPtr\<Aspose::Words::EditableRangeStart\>\&) | Marque la position actuelle dans le document comme la fin d'une plage modifiable. |
| [EndRow](./endrow/)() | Termine une ligne de tableau dans le document. |
| [EndTable](./endtable/)() | Termine un tableau dans le document. |
| [get_Bold](./get_bold/)() | Vrai si la police est formatée en gras. |
| [get_CellFormat](./get_cellformat/)() | Renvoie un objet qui représente les propriétés de formatage de la cellule de tableau actuelle. |
| [get_CurrentNode](./get_currentnode/)() | Obtient le nœud qui est actuellement sélectionné dans ce [DocumentBuilder](./). |
| [get_CurrentParagraph](./get_currentparagraph/)() | Obtient le paragraphe qui est actuellement sélectionné dans ce [DocumentBuilder](./). |
| [get_CurrentSection](./get_currentsection/)() | Obtient la section qui est actuellement sélectionnée dans ce [DocumentBuilder](./). |
| [get_CurrentStory](./get_currentstory/)() | Obtient l'histoire qui est actuellement sélectionnée dans ce [DocumentBuilder](./). |
| [get_CurrentStructuredDocumentTag](./get_currentstructureddocumenttag/)() | Obtient la balise de document structuré qui est actuellement sélectionnée dans ce [DocumentBuilder](./). |
| [get_Document](./get_document/)() const | Obtient ou définit l'objet [Document](./get_document/) auquel cet objet est attaché. |
| [get_Font](./get_font/)() | Renvoie un objet qui représente les propriétés de formatage de la police actuelle. |
| [get_IsAtEndOfParagraph](./get_isatendofparagraph/)() | Renvoie **true** si le curseur est à la fin du paragraphe actuel. |
| [get_IsAtEndOfStructuredDocumentTag](./get_isatendofstructureddocumenttag/)() | Renvoie **true** si le curseur est à la fin d'une balise de document structuré. |
| [get_IsAtStartOfParagraph](./get_isatstartofparagraph/)() | Renvoie **true** si le curseur est au début du paragraphe actuel (aucun texte avant le curseur). |
| [get_Italic](./get_italic/)() | Vrai si la police est formatée en italique. |
| [get_ListFormat](./get_listformat/)() | Renvoie un objet qui représente les propriétés de mise en forme de la liste actuelle. |
| [get_PageSetup](./get_pagesetup/)() | Renvoie un objet qui représente les paramètres de page et les propriétés de section actuels. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Renvoie un objet qui représente les propriétés de mise en forme du paragraphe actuel. |
| [get_RowFormat](./get_rowformat/)() | Renvoie un objet qui représente les propriétés de mise en forme de la ligne de tableau actuelle. |
| [get_Underline](./get_underline/)() | Obtient/définit le type de soulignement pour la police actuelle. |
| [GetType](./gettype/)() const override |  |
| [InsertBreak](./insertbreak/)(Aspose::Words::BreakType) | Insère un saut du type spécifié dans le document. |
| [InsertCell](./insertcell/)() | Insère une cellule de tableau dans le document. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, double, double) | Insère un objet de graphique dans le document et le redimensionne à la taille spécifiée. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, double, double, Aspose::Words::Drawing::Charts::ChartStyle) | Insère un objet de graphique dans le document et le redimensionne à la taille spécifiée. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Insère un objet de graphique dans le document et le redimensionne à la taille spécifiée. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType, Aspose::Words::Drawing::Charts::ChartStyle) | Insère un objet de graphique dans le document et le redimensionne à la taille spécifiée. |
| [InsertCheckBox](./insertcheckbox/)(const System::String\&, bool, int32_t) | Insère un champ de formulaire case à cocher à la position actuelle. |
| [InsertCheckBox](./insertcheckbox/)(const System::String\&, bool, bool, int32_t) | Insère un champ de formulaire case à cocher à la position actuelle. |
| [InsertComboBox](./insertcombobox/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, int32_t) | Insère un champ de formulaire combo box à la position actuelle. |
| [InsertDocument](./insertdocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) | Insère un document à la position du curseur. |
| [InsertDocument](./insertdocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Insère un document à la position du curseur. |
| [InsertDocumentInline](./insertdocumentinline/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Insère un document en ligne à la position du curseur. |
| [InsertField](./insertfield/)(Aspose::Words::Fields::FieldType, bool) | Insère un champ Word dans un document et met éventuellement à jour le résultat du champ. |
| [InsertField](./insertfield/)(const System::String\&) | Insère un champ Word dans un document et met à jour le résultat du champ. |
| [InsertField](./insertfield/)(const System::String\&, const System::String\&) | Insère un champ Word dans un document sans mettre à jour le résultat du champ. |
| [InsertFootnote](./insertfootnote/)(Aspose::Words::Notes::FootnoteType, const System::String\&) | Insère une note de bas de page ou une note de fin dans le document. |
| [InsertFootnote](./insertfootnote/)(Aspose::Words::Notes::FootnoteType, const System::String\&, const System::String\&) | Insère une note de bas de page ou une note de fin dans le document. |
| [InsertForms2OleControl](./insertforms2olecontrol/)(const System::SharedPtr\<Aspose::Words::Drawing::Ole::Forms2OleControl\>\&) | Insère l'objet [Forms2OleControl](../) à la position actuelle. |
| [InsertGroupShape](./insertgroupshape/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) | Regroupe les formes passées en paramètre dans un nouveau nœud GroupShape qui est inséré à la position actuelle. |
| [InsertGroupShape](./insertgroupshape/)(double, double, double, double, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) | Regroupe les formes passées en paramètre dans un nouveau nœud GroupShape de la taille spécifiée qui est inséré à la position spécifiée. |
| [InsertHorizontalRule](./inserthorizontalrule/)() | Insère une forme de règle horizontale dans le document. |
| [InsertHtml](./inserthtml/)(const System::String\&) | Insère une chaîne HTML dans le document. |
| [InsertHtml](./inserthtml/)(const System::String\&, bool) | Insère une chaîne HTML dans le document. |
| [InsertHtml](./inserthtml/)(const System::String\&, Aspose::Words::HtmlInsertOptions) | Insère une chaîne HTML dans le document. Permet de spécifier des options supplémentaires. |
| [InsertHyperlink](./inserthyperlink/)(const System::String\&, const System::String\&, bool) | Insère un hyperlien dans le document. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Insère une image à partir d'un objet **Image** dans le document. L'image est insérée en ligne et à 100 % d'échelle. |
| [InsertImage](./insertimage/)(const System::String\&) | Insère une image à partir d'un fichier ou d'une URL dans le document. L'image est insérée en ligne et à 100 % d'échelle. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | Insère une image à partir d'un flux dans le document. L'image est insérée en ligne et à 100 % d'échelle. |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&) | Insère une image à partir d'un tableau d'octets dans le document. L'image est insérée en ligne et à 100 % d'échelle. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, double, double) | Insère une image en ligne à partir d'un objet **Image** dans le document et la redimensionne à la taille spécifiée. |
| [InsertImage](./insertimage/)(const System::String\&, double, double) | Insère une image en ligne à partir d'un fichier ou d'une URL dans le document et la redimensionne à la taille spécifiée. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&, double, double) | Insère une image en ligne à partir d'un flux dans le document et la redimensionne à la taille spécifiée. |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&, double, double) | Insère une image en ligne à partir d'un tableau d'octets dans le document et la redimensionne à la taille spécifiée. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Insère une image à partir d'un objet **Image** à la position et à la taille spécifiées. |
| [InsertImage](./insertimage/)(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Insère une image à partir d'un fichier ou d'une URL à la position et à la taille spécifiées. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Insère une image à partir d'un flux à la position et à la taille spécifiées. |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Insère une image à partir d'un tableau d'octets à la position et à la taille spécifiées. |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&, double, double) |  |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) |  |
| [InsertNode](./insertnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Insère un nœud avant le curseur. |
| [InsertOleObject](./insertoleobject/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, bool, const System::SharedPtr\<System::IO::Stream\>\&) | Insère un objet OLE incorporé à partir d'un flux dans le document. |
| [InsertOleObject](./insertoleobject/)(const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) | Insère un objet OLE incorporé ou lié à partir d'un fichier dans le document. Détecte le type d'objet OLE à l'aide de l'extension du fichier. |
| [InsertOleObject](./insertoleobject/)(const System::String\&, const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) | Insère un objet OLE incorporé ou lié à partir d'un fichier dans le document. Détecte le type d'objet OLE à l'aide du paramètre progID fourni. |
| [InsertOleObject](./insertoleobject/)(std::basic_istream\<CharType, Traits\>\&, System::String, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObject](./insertoleobject/)(System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObject](./insertoleobject/)(System::String, System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::String\&, bool, const System::String\&, const System::String\&) | Insère un objet OLE incorporé ou lié sous forme d'icône dans le document. Permet de spécifier le fichier d'icône et la légende. Détecte le type d'objet OLE à l'aide de l'extension du fichier. |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::String\&, const System::String\&, bool, const System::String\&, const System::String\&) | Insère un objet OLE incorporé ou lié sous forme d'icône dans le document. Permet de spécifier le fichier d'icône et la légende. Détecte le type d'objet OLE à l'aide du paramètre progID fourni. |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, const System::String\&, const System::String\&) | Insère un objet OLE incorporé sous forme d'icône à partir d'un flux dans le document. Permet de spécifier le fichier d'icône et la légende. Détecte le type d'objet OLE à l'aide du paramètre progID fourni. |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(std::basic_istream\<CharType, Traits\>\&, System::String, System::String, System::String) |  |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, double, double) | Insère un objet vidéo en ligne dans le document et le redimensionne à la taille spécifiée. |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Insère un objet vidéo en ligne dans le document et le redimensionne à la taille spécifiée. |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, double, double) | Insère un objet vidéo en ligne dans le document et le redimensionne à la taille spécifiée. |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Insère un objet vidéo en ligne dans le document et le redimensionne à la taille spécifiée. |
| [InsertParagraph](./insertparagraph/)() | Insère un saut de paragraphe dans le document. |
| [InsertShape](./insertshape/)(Aspose::Words::Drawing::ShapeType, double, double) | Insère une forme en ligne avec le type et la taille spécifiés. |
| [InsertShape](./insertshape/)(Aspose::Words::Drawing::ShapeType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Insère une forme flottante avec la position, la taille et le type d'habillage du texte spécifiés. |
| [InsertSignatureLine](./insertsignatureline/)(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&) | Insère une ligne de signature à la position actuelle. |
| [InsertSignatureLine](./insertsignatureline/)(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, Aspose::Words::Drawing::WrapType) | Insère une ligne de signature à la position spécifiée. |
| [InsertStructuredDocumentTag](./insertstructureddocumenttag/)(Aspose::Words::Markup::SdtType) | Insère un [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/) dans le document. |
| [InsertStyleSeparator](./insertstyleseparator/)() | Insère un séparateur de style dans le document. |
| [InsertTableOfContents](./inserttableofcontents/)(const System::String\&) | Insère un champ TOC (table des matières) dans le document. |
| [InsertTextInput](./inserttextinput/)(const System::String\&, Aspose::Words::Fields::TextFormFieldType, const System::String\&, const System::String\&, int32_t) | Insère un champ de formulaire texte à la position actuelle. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MoveTo](./moveto/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Déplace le curseur vers un nœud en ligne ou vers la fin d'un paragraphe. |
| [MoveToBookmark](./movetobookmark/)(const System::String\&) | Déplace le curseur vers un signet. |
| [MoveToBookmark](./movetobookmark/)(const System::String\&, bool, bool) | Déplace le curseur vers un signet avec une plus grande précision. |
| [MoveToCell](./movetocell/)(int32_t, int32_t, int32_t, int32_t) | Déplace le curseur vers une cellule de tableau dans la section actuelle. |
| [MoveToDocumentEnd](./movetodocumentend/)() | Déplace le curseur vers la fin du document. |
| [MoveToDocumentStart](./movetodocumentstart/)() | Déplace le curseur vers le début du document. |
| [MoveToField](./movetofield/)(const System::SharedPtr\<Aspose::Words::Fields::Field\>\&, bool) | Déplace le curseur vers un champ dans le document. |
| [MoveToHeaderFooter](./movetoheaderfooter/)(Aspose::Words::HeaderFooterType) | Déplace le curseur vers le début d'un en-tête ou d'un pied de page dans la section actuelle. |
| [MoveToMergeField](./movetomergefield/)(const System::String\&) | Déplace le curseur vers une position juste après le champ de fusion spécifié et supprime le champ de fusion. |
| [MoveToMergeField](./movetomergefield/)(const System::String\&, bool, bool) | Déplace le champ de fusion vers le champ de fusion spécifié. |
| [MoveToParagraph](./movetoparagraph/)(int32_t, int32_t) | Déplace le curseur vers un paragraphe dans la section actuelle. |
| [MoveToSection](./movetosection/)(int32_t) | Déplace le curseur vers le début du corps dans une section spécifiée. |
| [MoveToStructuredDocumentTag](./movetostructureddocumenttag/)(int32_t, int32_t) | Déplace le curseur vers une balise de document structuré dans la section actuelle. |
| [MoveToStructuredDocumentTag](./movetostructureddocumenttag/)(const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\&, int32_t) | Déplace le curseur vers la balise de document structuré. |
| [PopFont](./popfont/)() | Récupère le formatage de caractères précédemment enregistré sur la pile. |
| [PushFont](./pushfont/)() | Enregistre le formatage de caractères actuel sur la pile. |
| [set_Bold](./set_bold/)(bool) | Définisseur pour [Aspose::Words::DocumentBuilder::get_Bold](./get_bold/). |
| [set_Document](./set_document/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Définisseur pour [Aspose::Words::DocumentBuilder::get_Document](./get_document/). |
| [set_Italic](./set_italic/)(bool) | Définisseur pour [Aspose::Words::DocumentBuilder::get_Italic](./get_italic/). |
| [set_Underline](./set_underline/)(Aspose::Words::Underline) | Définisseur pour [Aspose::Words::DocumentBuilder::get_Underline](./get_underline/). |
| [StartBookmark](./startbookmark/)(const System::String\&) | Marque la position actuelle dans le document comme le début d'un signet. |
| [StartColumnBookmark](./startcolumnbookmark/)(const System::String\&) | Marque la position actuelle dans le document comme le début d'un signet de colonne. La position doit être dans une cellule de tableau. |
| [StartEditableRange](./starteditablerange/)() | Marque la position actuelle dans le document comme le début d'une plage modifiable. |
| [StartTable](./starttable/)() | Démarre un tableau dans le document. |
| static [Type](./type/)() |  |
| [Write](./write/)(const System::String\&) | Insère une chaîne dans le document à la position d'insertion actuelle. |
| [Writeln](./writeln/)(const System::String\&) | Insère une chaîne et un saut de paragraphe dans le document. |
| [Writeln](./writeln/)() | Insère un saut de paragraphe dans le document. |
## Remarques


[DocumentBuilder](./) makes the process of building a [Document](../document/) easier. [Document](../document/) is a composite object consisting of a tree of nodes and while inserting content nodes directly into the tree is possible, it requires good understanding of the tree structure. [DocumentBuilder](./) is a "facade" for the complex structure of [Document](../document/) and allows to insert content and formatting quickly and easily.

Créez un [DocumentBuilder](./) et associez-le à un [Document](../document/).

Le [DocumentBuilder](./) possède un curseur interne où le texte sera inséré lorsque vous appelez [Write()](../), [Writeln()](../), [InsertBreak()](./insertbreak/) et d'autres méthodes. Vous pouvez déplacer le curseur du [DocumentBuilder](./) vers un autre emplacement dans un document en utilisant diverses méthodes MoveToXXX.

Utilisez la propriété [Font](./get_font/) pour spécifier le formatage des caractères qui s'appliquera à tout le texte inséré à partir de la position actuelle dans le document.

Utilisez la propriété [ParagraphFormat](./get_paragraphformat/) pour spécifier le formatage des paragraphes pour le paragraphe actuel et tous les paragraphes qui seront insérés.

Utilisez la propriété [PageSetup](./get_pagesetup/) pour spécifier les propriétés de page et de section pour la section actuelle et toutes les sections qui seront insérées.

Utilisez les propriétés [CellFormat](./get_cellformat/) et [RowFormat](./get_rowformat/) pour spécifier les propriétés de formatage des cellules et des lignes de tableau. Utilisez les méthodes [InsertCell](./insertcell/) et [EndRow](./endrow/) pour construire un tableau.

Notez que les propriétés [Font](./get_font/), [ParagraphFormat](./get_paragraphformat/) et [PageSetup](./get_pagesetup/) sont mises à jour chaque fois que vous naviguez vers un autre endroit du document afin de refléter les propriétés de formatage disponibles à la nouvelle position.

## Exemples



Montre comment construire un tableau avec des bordures personnalisées.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// Définition des options de formatage de tableau pour un DocumentBuilder
// les appliquera à chaque ligne et cellule que nous ajoutons avec celui‑ci.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Engrave3D);
builder->get_RowFormat()->get_Borders()->set_Color(System::Drawing::Color::get_Orange());

builder->InsertCell();
builder->Write(u"Row 1, Col 1");

builder->InsertCell();
builder->Write(u"Row 1, Col 2");
builder->EndRow();

// Modifier le formatage l'appliquera à la cellule actuelle,
// et à toutes les nouvelles cellules que nous créons avec le constructeur par la suite.
// Cela n'affectera pas les cellules que nous avons ajoutées précédemment.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// Augmentez la hauteur de la ligne pour adapter le texte vertical.
builder->InsertCell();
builder->get_RowFormat()->set_Height(150);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTable.docx");
```


Montre comment utiliser un DocumentBuilder pour créer un tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Démarrez le tableau, puis remplissez la première ligne avec deux cellules.
builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");

// Appelez la méthode "EndRow" du constructeur pour démarrer une nouvelle ligne.
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateTable.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
