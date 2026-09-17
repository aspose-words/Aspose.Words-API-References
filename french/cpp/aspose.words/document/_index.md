---
title: "Classe Aspose::Words::Document"
linktitle: "Document"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Document. Représente un document Word. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 20000
url: /fr/cpp/aspose.words/document/
---
## Document class


Représente un document Word. Pour en savoir plus, consultez l'article de documentation [Working with Document](https://docs.aspose.com/words/cpp/working-with-document/).

```cpp
class Document : public Aspose::Words::DocumentBase,
                 public Aspose::Words::ISectionAttrSource,
                 public Aspose::Words::IWatermarkProvider
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur. |
| [AcceptAllRevisions](./acceptallrevisions/)() | Accepte toutes les modifications suivies dans le document. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur pour visiter la fin du document. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur pour visiter le début du document. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendDocument](./appenddocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) | Ajoute le document spécifié à la fin de ce document. |
| [AppendDocument](./appenddocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Ajoute le document spécifié à la fin de ce document. |
| [Cleanup](./cleanup/)() | Nettoie les styles et listes inutilisés du document. |
| [Cleanup](./cleanup/)(const System::SharedPtr\<Aspose::Words::CleanupOptions\>\&) | Nettoie les styles et listes inutilisés du document en fonction des [CleanupOptions](../cleanupoptions/) fournis. |
| [Clone](./clone/)() | Effectue une copie profonde du [Document](./). |
| [Clone](../node/clone/)(bool) | Crée un duplicata du nœud. |
| [Compare](./compare/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::String\&, System::DateTime) | Compare ce document avec un autre document en produisant des changements sous forme de nombre de révisions d'édition et de format [Revision](../revision/). |
| [Compare](./compare/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compare ce document avec un autre document en produisant des changements sous forme d'un nombre de révisions d'édition et de format [Revision](../revision/). Permet de spécifier des options de comparaison en utilisant [CompareOptions](../../aspose.words.comparing/compareoptions/). |
| [CopyStylesFromTemplate](./copystylesfromtemplate/)(const System::String\&) | Copie les styles du modèle spécifié vers un document. |
| [CopyStylesFromTemplate](./copystylesfromtemplate/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Copie les styles du modèle spécifié vers un document. |
| [Document](./document/)() | Crée un document Word vierge. |
| [Document](./document/)(const System::String\&) | Ouvre un document existant à partir d'un fichier. Détecte automatiquement le format du fichier. |
| [Document](./document/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Ouvre un document existant à partir d'un fichier. Permet de spécifier des options supplémentaires telles qu'un mot de passe de chiffrement. |
| [Document](./document/)(const System::SharedPtr\<System::IO::Stream\>\&) | Ouvre un document existant à partir d'un flux. Détecte automatiquement le format du fichier. |
| [Document](./document/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Ouvre un document existant à partir d'un flux. Permet de spécifier des options supplémentaires telles qu'un mot de passe de chiffrement. |
| [Document](./document/)(std::istream\&) |  |
| [Document](./document/)(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) |  |
| [EnsureMinimum](./ensureminimum/)() | Si le document ne contient aucune section, crée une section avec un paragraphe. |
| [ExpandTableStylesToDirectFormatting](./expandtablestylestodirectformatting/)() | Convertit le formatage spécifié dans les styles de tableau en formatage direct sur les tableaux du document. |
| [ExtractPages](./extractpages/)(int32_t, int32_t, const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\&) | Renvoie l'objet [Document](./) représentant la plage de pages spécifiée et les options d'extraction de page données. |
| [ExtractPages](./extractpages/)(int32_t, int32_t) | Renvoie l'objet [Document](./) représentant la plage de pages spécifiée. |
| [get_AttachedTemplate](./get_attachedtemplate/)() | Obtient ou définit le chemin complet du modèle attaché au document. |
| [get_AutomaticallyUpdateStyles](./get_automaticallyupdatestyles/)() | Obtient ou définit un indicateur indiquant si les styles du document sont mis à jour pour correspondre aux styles du modèle attaché chaque fois que le document est ouvert dans MS Word. |
| [get_BackgroundShape](../documentbase/get_backgroundshape/)() const | Obtient ou définit la forme d'arrière-plan du document. Peut être **null**. |
| [get_Bibliography](./get_bibliography/)() | Obtient l'objet [Bibliography](./get_bibliography/) qui représente la liste des sources disponibles dans le document. |
| [get_BuiltInDocumentProperties](./get_builtindocumentproperties/)() const | Renvoie une collection qui représente toutes les propriétés intégrées du document. |
| [get_CompatibilityOptions](./get_compatibilityoptions/)() | Fournit l'accès aux options de compatibilité du document (c’est‑à‑dire les préférences utilisateur saisies dans l'onglet **Compatibility** de la boîte de dialogue **Options** de Word). |
| [get_Compliance](./get_compliance/)() | Obtient la version de conformité OOXML déterminée à partir du contenu du document chargé. N’a de sens que pour les documents OOXML. |
| [get_Count](../compositenode/get_count/)() | Obtient le nombre d'enfants immédiats de ce nœud. |
| [get_CustomDocumentProperties](./get_customdocumentproperties/)() | Renvoie une collection qui représente toutes les propriétés personnalisées du document. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Spécifie un identifiant de nœud personnalisé. |
| [get_CustomXmlParts](./get_customxmlparts/)() const | Obtient ou définit la collection des parties de stockage de données XML personnalisées. |
| [get_DefaultTabStop](./get_defaulttabstop/)() | Obtient ou définit l'intervalle (en points) entre les tabulations par défaut. |
| [get_DigitalSignatures](./get_digitalsignatures/)() const | Obtient la collection des signatures numériques de ce document et leurs résultats de validation. |
| [get_Document](../documentbase/get_document/)() const override | Obtient cette instance. |
| [get_EndnoteOptions](./get_endnoteoptions/)() | Fournit des options qui contrôlent la numérotation et le positionnement des notes de fin dans ce document. |
| [get_FieldOptions](./get_fieldoptions/)() | Obtient un objet [FieldOptions](../../aspose.words.fields/fieldoptions/) qui représente les options de contrôle du traitement des champs dans le document. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Obtient le premier enfant du nœud. |
| [get_FirstSection](./get_firstsection/)() | Obtient la première section du document. |
| [get_FontInfos](../documentbase/get_fontinfos/)() const | Fournit l'accès aux propriétés des polices utilisées dans ce document. |
| [get_FontSettings](./get_fontsettings/)() const | Obtient ou définit les paramètres de police du document. |
| [get_FootnoteOptions](./get_footnoteoptions/)() | Fournit des options qui contrôlent la numérotation et le positionnement des notes de bas de page dans ce document. |
| [get_FootnoteSeparators](../documentbase/get_footnoteseparators/)() const | Fournit l'accès aux séparateurs de notes de bas de page/notes de fin définis dans le document. |
| [get_Frameset](./get_frameset/)() const | Renvoie une instance [Frameset](./get_frameset/) si ce document représente une page à cadres. |
| [get_GlossaryDocument](./get_glossarydocument/)() const | Obtient ou définit le document de glossaire dans ce document ou modèle. Un document de glossaire est un stockage pour les entrées AutoText, AutoCorrect et Building Block définies dans un document. |
| [get_GrammarChecked](./get_grammarchecked/)() | Renvoie **true** si le document a été vérifié pour la grammaire. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Renvoie **true** si ce nœud possède des nœuds enfants. |
| [get_HasMacros](./get_hasmacros/)() | Renvoie **true** si le document possède un projet VBA (macros). |
| [get_HasRevisions](./get_hasrevisions/)() | Renvoie **true** si le document comporte des modifications suivies. |
| [get_HyphenationOptions](./get_hyphenationoptions/)() | Fournit l'accès aux options de césure du document. |
| [get_IncludeTextboxesFootnotesEndnotesInStat](./get_includetextboxesfootnotesendnotesinstat/)() | Spécifie s'il faut inclure les zones de texte, les notes de bas de page et les notes de fin dans les statistiques de comptage de mots. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Renvoie **true** car ce nœud peut avoir des nœuds enfants. |
| [get_JustificationMode](./get_justificationmode/)() | Obtient ou définit le réglage de l'espacement des caractères d'un document. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Obtient le dernier enfant du nœud. |
| [get_LastSection](./get_lastsection/)() | Obtient la dernière section du document. |
| [get_LayoutOptions](./get_layoutoptions/)() const | Obtient un objet [LayoutOptions](../../aspose.words.layout/layoutoptions/) qui représente les options permettant de contrôler le processus de mise en page de ce document. |
| [get_Lists](../documentbase/get_lists/)() const | Fournit l'accès au formatage des listes utilisé dans le document. |
| [get_MailMerge](./get_mailmerge/)() | Renvoie un objet [MailMerge](../../aspose.words.mailmerging/mailmerge/) qui représente la fonctionnalité de publipostage pour le document. |
| [get_MailMergeSettings](./get_mailmergesettings/)() | Obtient ou définit l'objet qui contient toutes les informations de publipostage d'un document. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Obtient le nœud immédiatement suivant ce nœud. |
| [get_NodeChangingCallback](../documentbase/get_nodechangingcallback/)() | Appelé lorsqu'un nœud est inséré ou supprimé dans le document. |
| [get_NodeType](./get_nodetype/)() const override | Renvoie [Document](../nodetype/). |
| [get_OriginalFileName](./get_originalfilename/)() const | Obtient le nom de fichier original du document. |
| [get_OriginalLoadFormat](./get_originalloadformat/)() const | Obtient le format du document original qui a été chargé dans cet objet. |
| [get_PackageCustomParts](./get_packagecustomparts/)() const | Obtient ou définit la collection de parties personnalisées (contenu arbitraire) qui sont liées au package OOXML à l'aide de « relations inconnues ». |
| [get_PageColor](../documentbase/get_pagecolor/)() | Obtient ou définit la couleur de page du document. Cette propriété est une version simplifiée de [BackgroundShape](../documentbase/get_backgroundshape/). |
| [get_PageCount](./get_pagecount/)() | Obtient le nombre de pages du document tel que calculé par la dernière opération de mise en page. |
| [get_ParentNode](../node/get_parentnode/)() | Obtient le parent immédiat de ce nœud. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Obtient le nœud immédiatement précédent ce nœud. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_ProtectionType](./get_protectiontype/)() | Obtient le type de protection du document actuellement actif. |
| [get_PunctuationKerning](./get_punctuationkerning/)() | Spécifie si le crénage s'applique à la fois au texte latin et à la ponctuation. |
| [get_Range](../node/get_range/)() | Renvoie un objet [Range](../range/) qui représente la partie d'un document contenue dans ce nœud. |
| [get_ReadabilityStatistics](./get_readabilitystatistics/)() | Fournit des informations sur le score de lisibilité du document. |
| [get_RemovePersonalInformation](./get_removepersonalinformation/)() | Obtient ou définit un indicateur indiquant que Microsoft Word supprimera toutes les informations utilisateur des commentaires, révisions et propriétés du document lors de l'enregistrement du document. |
| [get_ResourceLoadingCallback](../documentbase/get_resourceloadingcallback/)() const | Permet de contrôler la façon dont les ressources externes sont chargées. |
| [get_Revisions](./get_revisions/)() | Obtient une collection de révisions (modifications suivies) qui existent dans ce document. |
| [get_RevisionsView](./get_revisionsview/)() const | Obtient ou définit une valeur indiquant s'il faut travailler avec la version originale ou révisée d'un document. |
| [get_Sections](./get_sections/)() | Renvoie une collection qui représente toutes les sections du document. |
| [get_ShadeFormData](./get_shadeformdata/)() | Spécifie s'il faut activer l'ombrage gris sur les champs de formulaire. |
| [get_ShowGrammaticalErrors](./get_showgrammaticalerrors/)() | Spécifie s'il faut afficher les erreurs grammaticales dans ce document. |
| [get_ShowSpellingErrors](./get_showspellingerrors/)() | Spécifie s'il faut afficher les fautes d'orthographe dans ce document. |
| [get_SpellingChecked](./get_spellingchecked/)() | Renvoie **true** si le document a été vérifié pour l'orthographe. |
| [get_Styles](../documentbase/get_styles/)() const | Renvoie une collection de styles définis dans le document. |
| [get_Theme](./get_theme/)() | Obtient l'objet [Theme](./get_theme/) de ce document. |
| [get_TrackRevisions](./get_trackrevisions/)() | Vrai si les modifications sont suivies lorsque ce document est modifié dans Microsoft Word. |
| [get_Variables](./get_variables/)() | Renvoie la collection de variables ajoutées à un document ou à un modèle. |
| [get_VbaProject](./get_vbaproject/)() const | Obtient ou définit un [VbaProject](./get_vbaproject/). |
| [get_VersionsCount](./get_versionscount/)() | Obtient le nombre de versions du document qui ont été stockées dans le document DOC. |
| [get_ViewOptions](./get_viewoptions/)() | Fournit des options pour contrôler la façon dont le document est affiché dans Microsoft Word. |
| [get_WarningCallback](../documentbase/get_warningcallback/)() const | Appelé pendant diverses procédures de traitement de document lorsqu'un problème est détecté pouvant entraîner une perte de fidélité des données ou du formatage. |
| [get_Watermark](./get_watermark/)() | Fournit l'accès au filigrane du document. |
| [get_WebExtensionTaskPanes](./get_webextensiontaskpanes/)() const | Renvoie une collection qui représente une liste de modules complémentaires du volet des tâches. |
| [get_WriteProtection](./get_writeprotection/)() | Fournit l'accès aux options de protection en écriture du document. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Obtient le premier ancêtre du [NodeType](../nodetype/) spécifié. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Renvoie le nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Renvoie une collection dynamique de nœuds enfants qui correspondent au type spécifié. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Fournit une prise en charge de l'itération de type foreach sur les nœuds enfants de ce nœud. |
| [GetPageInfo](./getpageinfo/)(int32_t) | Obtient la taille de la page, l'orientation et d'autres informations sur une page qui pourraient être utiles pour l'impression ou le rendu. |
| [GetText](../compositenode/gettext/)() override | Obtient le texte de ce nœud et de tous ses enfants. |
| [GetType](./gettype/)() const override |  |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Importe un nœud d'un autre document vers le document actuel. |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) | Importe un nœud d'un autre document vers le document actuel avec une option pour contrôler le formatage. |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Importe un nœud d'un autre document vers le document actuel avec une option pour contrôler le formatage. |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Renvoie l'index du nœud enfant spécifié dans le tableau des nœuds enfants. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)() | Fusionne les séquences avec le même formatage dans tous les paragraphes du document. |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud suivant selon l'algorithme de traversée d'arbre en pré-ordre. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Méthode utilitaire qui convertit une valeur d'énumération de type de nœud en une chaîne conviviale. |
| [NormalizeFieldTypes](./normalizefieldtypes/)() | Modifie les valeurs du type de champ [FieldType](../../aspose.words.fields/fieldchar/get_fieldtype/) de [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/) et [FieldEnd](../../aspose.words.fields/fieldend/) dans l'ensemble du document afin qu'elles correspondent aux types de champ contenus dans les codes de champ. |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud précédent selon l'algorithme de traversée d'arbre en pré-ordre. |
| [Protect](./protect/)(Aspose::Words::ProtectionType) | Protège le document contre les modifications sans changer le mot de passe existant ou attribue un mot de passe aléatoire. |
| [Protect](./protect/)(Aspose::Words::ProtectionType, const System::String\&) | Protège le document contre les modifications et définit éventuellement un mot de passe de protection. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Supprime tous les nœuds enfants du nœud actuel. |
| [RemoveBlankPages](./removeblankpages/)() | Supprime les pages blanches du document. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveCustomizations](./removecustomizations/)() | Supprime les personnalisations de la barre d'outils et des raccourcis clavier du document. |
| [RemoveExternalSchemaReferences](./removeexternalschemareferences/)() | Supprime les références de schémas XML externes de ce document. |
| [RemoveMacros](./removemacros/)() | Supprime toutes les macros (le projet VBA) ainsi que les barres d'outils et les personnalisations de commandes du document. |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Supprime tous les nœuds descendants [SmartTag](../../aspose.words.markup/smarttag/) du nœud actuel. |
| [RenderToScale](./rendertoscale/)(int32_t, const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | Rend une page de document dans un objet **Graphics** à une échelle spécifiée. |
| [RenderToSize](./rendertosize/)(int32_t, const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | Rend une page de document dans un objet **Graphics** à une taille spécifiée. |
| [Save](./save/)(const System::String\&) | Enregistre le document dans un fichier. Détermine automatiquement le format d'enregistrement à partir de l'extension. |
| [Save](./save/)(const System::String\&, Aspose::Words::SaveFormat) | Enregistre le document dans un fichier au format spécifié. |
| [Save](./save/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Enregistre le document dans un fichier en utilisant les options d'enregistrement spécifiées. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Enregistre le document dans un flux en utilisant le format spécifié. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Enregistre le document dans un flux en utilisant les options d'enregistrement spécifiées. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, Aspose::Words::SaveFormat) |  |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) |  |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Sélectionne le premier [Node](../node/) qui correspond à l'expression XPath. |
| [set_AttachedTemplate](./set_attachedtemplate/)(const System::String\&) | Définisseur de [Aspose::Words::Document::get_AttachedTemplate](./get_attachedtemplate/). |
| [set_AutomaticallyUpdateStyles](./set_automaticallyupdatestyles/)(bool) | Définisseur de [Aspose::Words::Document::get_AutomaticallyUpdateStyles](./get_automaticallyupdatestyles/). |
| [set_BackgroundShape](../documentbase/set_backgroundshape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | Définisseur de [Aspose::Words::DocumentBase::get_BackgroundShape](../documentbase/get_backgroundshape/). |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Définisseur pour [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_CustomXmlParts](./set_customxmlparts/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPartCollection\>\&) | Définisseur de [Aspose::Words::Document::get_CustomXmlParts](./get_customxmlparts/). |
| [set_DefaultTabStop](./set_defaulttabstop/)(double) | Définisseur de [Aspose::Words::Document::get_DefaultTabStop](./get_defaulttabstop/). |
| [set_FontSettings](./set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Définisseur de [Aspose::Words::Document::get_FontSettings](./get_fontsettings/). |
| [set_GlossaryDocument](./set_glossarydocument/)(const System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>\&) | Définisseur de [Aspose::Words::Document::get_GlossaryDocument](./get_glossarydocument/). |
| [set_GrammarChecked](./set_grammarchecked/)(bool) | Définisseur de [Aspose::Words::Document::get_GrammarChecked](./get_grammarchecked/). |
| [set_IncludeTextboxesFootnotesEndnotesInStat](./set_includetextboxesfootnotesendnotesinstat/)(bool) | Définisseur de [Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat](./get_includetextboxesfootnotesendnotesinstat/). |
| [set_JustificationMode](./set_justificationmode/)(Aspose::Words::Settings::JustificationMode) | Définisseur de [Aspose::Words::Document::get_JustificationMode](./get_justificationmode/). |
| [set_MailMergeSettings](./set_mailmergesettings/)(const System::SharedPtr\<Aspose::Words::Settings::MailMergeSettings\>\&) | Définisseur de [Aspose::Words::Document::get_MailMergeSettings](./get_mailmergesettings/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_NodeChangingCallback](../documentbase/set_nodechangingcallback/)(const System::SharedPtr\<Aspose::Words::INodeChangingCallback\>\&) | Appelé lorsqu'un nœud est inséré ou supprimé dans le document. |
| [set_PackageCustomParts](./set_packagecustomparts/)(const System::SharedPtr\<Aspose::Words::Markup::CustomPartCollection\>\&) | Définisseur de [Aspose::Words::Document::get_PackageCustomParts](./get_packagecustomparts/). |
| [set_PageColor](../documentbase/set_pagecolor/)(System::Drawing::Color) | Définisseur de [Aspose::Words::DocumentBase::get_PageColor](../documentbase/get_pagecolor/). |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PunctuationKerning](./set_punctuationkerning/)(bool) | Définisseur de [Aspose::Words::Document::get_PunctuationKerning](./get_punctuationkerning/). |
| [set_RemovePersonalInformation](./set_removepersonalinformation/)(bool) | Définisseur de [Aspose::Words::Document::get_RemovePersonalInformation](./get_removepersonalinformation/). |
| [set_ResourceLoadingCallback](../documentbase/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Permet de contrôler la façon dont les ressources externes sont chargées. |
| [set_RevisionsView](./set_revisionsview/)(Aspose::Words::RevisionsView) | Définisseur de [Aspose::Words::Document::get_RevisionsView](./get_revisionsview/). |
| [set_ShadeFormData](./set_shadeformdata/)(bool) | Définisseur de [Aspose::Words::Document::get_ShadeFormData](./get_shadeformdata/). |
| [set_ShowGrammaticalErrors](./set_showgrammaticalerrors/)(bool) | Définisseur de [Aspose::Words::Document::get_ShowGrammaticalErrors](./get_showgrammaticalerrors/). |
| [set_ShowSpellingErrors](./set_showspellingerrors/)(bool) | Définisseur de [Aspose::Words::Document::get_ShowSpellingErrors](./get_showspellingerrors/). |
| [set_SpellingChecked](./set_spellingchecked/)(bool) | Définisseur de [Aspose::Words::Document::get_SpellingChecked](./get_spellingchecked/). |
| [set_TrackRevisions](./set_trackrevisions/)(bool) | Définisseur de [Aspose::Words::Document::get_TrackRevisions](./get_trackrevisions/). |
| [set_VbaProject](./set_vbaproject/)(const System::SharedPtr\<Aspose::Words::Vba::VbaProject\>\&) | Définisseur de [Aspose::Words::Document::get_VbaProject](./get_vbaproject/). |
| [set_WarningCallback](../documentbase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Définisseur pour [Aspose::Words::DocumentBase::get_WarningCallback](../documentbase/get_warningcallback/). |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [StartTrackRevisions](./starttrackrevisions/)(const System::String\&, System::DateTime) | Commence automatiquement à marquer toutes les modifications ultérieures que vous apportez au document par programmation comme des modifications de révision. |
| [StartTrackRevisions](./starttrackrevisions/)(const System::String\&) | Commence automatiquement à marquer toutes les modifications ultérieures que vous apportez au document par programmation comme des modifications de révision. |
| [StopTrackRevisions](./stoptrackrevisions/)() | Arrête le marquage automatique des modifications du document en tant que révisions. |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporte le contenu du nœud dans une chaîne en utilisant les options d'enregistrement spécifiées. |
| static [Type](./type/)() |  |
| [UnlinkFields](./unlinkfields/)() | Délie les champs dans l'ensemble du document. |
| [Unprotect](./unprotect/)() | Supprime la protection du document quel que soit le mot de passe. |
| [Unprotect](./unprotect/)(const System::String\&) | Supprime la protection du document si un mot de passe correct est spécifié. |
| [UpdateActualReferenceMarks](./updateactualreferencemarks/)() | Met à jour la propriété [ActualReferenceMark](../../aspose.words.notes/footnote/get_actualreferencemark/) de toutes les notes de bas de page et notes de fin dans le document. |
| [UpdateFields](./updatefields/)() | Met à jour les valeurs des champs dans l'ensemble du document. |
| [UpdateListLabels](./updatelistlabels/)() | Met à jour les libellés de liste pour tous les éléments de liste dans le document. |
| [UpdatePageLayout](./updatepagelayout/)() | Reconstruit la mise en page du document. |
| [UpdateTableLayout](./updatetablelayout/)() | Implémente une approche antérieure du recalcul des largeurs de colonnes de tableau qui présente des problèmes connus. |
| [UpdateThumbnail](./updatethumbnail/)(const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\&) | Met à jour la [Thumbnail](../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) du document selon les options spécifiées. |
| [UpdateThumbnail](./updatethumbnail/)() | Met à jour la [Thumbnail](../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) du document en utilisant les options par défaut. |
| [UpdateWordCount](./updatewordcount/)() | Met à jour les propriétés de comptage de mots du document. |
| [UpdateWordCount](./updatewordcount/)(bool) | Met à jour les propriétés de comptage de mots du document, met éventuellement à jour la propriété [Lines](../../aspose.words.properties/builtindocumentproperties/get_lines/). |
## Remarques


Le [Document](./) est un objet central dans la bibliothèque Aspose.Words.

Pour charger un document existant dans l'un des formats [LoadFormat](../loadformat/), transmettez un nom de fichier ou un flux à l'un des constructeurs du [Document](./). Pour créer un document vierge, appelez le constructeur sans paramètres.

Utilisez l'une des surcharges de la méthode Save pour enregistrer le document dans l'un des formats [SaveFormat](../saveformat/).

Pour dessiner les pages du document directement sur un objet **Graphics**, utilisez la méthode [RenderToScale()](../) ou [RenderToSize()](../).

Pour imprimer le document, utilisez l'une des méthodes [Print()](../).

[MailMerge](./get_mailmerge/) is the [Aspose.Words](../)'s reporting engine that allows to populate reports designed in Microsoft Word with data from various data sources quickly and easily. The data can be from a or an array of values. **MailMerge** will go through the records found in the data source and insert them into mail merge fields in the document growing it as necessary.

[Document](./) stores document-wide information such as [Styles](../documentbase/get_styles/), [BuiltInDocumentProperties](./get_builtindocumentproperties/), [CustomDocumentProperties](./get_customdocumentproperties/), lists and macros. Most of these objects are accessible via the corresponding properties of the [Document](./).

Le [Document](./) est un nœud racine d'un arbre qui contient tous les autres nœuds du document. L'arbre suit le pattern de conception Composite et ressemble à bien des égards à XmlDocument. Le contenu du document peut être manipulé librement par programmation :

* The nodes of the document can be accessed via typed collections, for example [Sections](./get_sections/), [ParagraphCollection](../paragraphcollection/) etc.
* The nodes of the document can be selected by their node type using [GetChildNodes()](../compositenode/getchildnodes/) or using an XPath query with [SelectNodes()](../) or [SelectSingleNode()](../).
* Content nodes can be added or removed from anywhere in the document using [InsertBefore1()</see>, <see cref="Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertAfter1()](../), [RemoveChild``1()](../) and other methods provided by the base class [CompositeNode](../compositenode/).
* The formatting attributes of each node can be changed via the properties of that node.



Envisagez d'utiliser [DocumentBuilder](../documentbuilder/) qui simplifie la tâche de création ou de remplissage de l'arbre du document par programmation.

Le [Document](./) ne peut contenir que des objets [Section](../section/).

Dans Microsoft Word, un document valide doit contenir au moins une section.
## Voir aussi

* Class [DocumentBase](../documentbase/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
