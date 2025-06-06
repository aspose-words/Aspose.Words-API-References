---
title: Document Class
linktitle: Document
articleTitle: Document
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Document pour une manipulation fluide des documents Word. Optimisez vos projets grâce à des fonctionnalités puissantes et une intégration facile.
type: docs
weight: 640
url: /fr/net/aspose.words/document/
---
## Document class

Représente un document Word.

Pour en savoir plus, visitez le[Travailler avec un document](https://docs.aspose.com/words/net/working-with-document/) article de documentation.

```csharp
public class Document : DocumentBase
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [Document](document/#constructor)() | Crée un document Word vierge. |
| [Document](document/#constructor_1)(*Stream*) | Ouvre un document existant à partir d'un flux. Détecte automatiquement le format du fichier. |
| [Document](document/#constructor_3)(*string*) | Ouvre un document existant à partir d'un fichier. Détecte automatiquement le format du fichier. |
| [Document](document/#constructor_2)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Ouvre un document existant depuis un flux. Permet de spécifier des options supplémentaires, comme un mot de passe de chiffrement. |
| [Document](document/#constructor_4)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Ouvre un document existant à partir d'un fichier. Permet de spécifier des options supplémentaires, comme un mot de passe de chiffrement. |

## Propriétés

| Nom | La description |
| --- | --- |
| [AttachedTemplate](../../aspose.words/document/attachedtemplate/) { get; set; } | Obtient ou définit le chemin complet du modèle attaché au document. |
| [AutomaticallyUpdateStyles](../../aspose.words/document/automaticallyupdatestyles/) { get; set; } | Obtient ou définit un indicateur indiquant si les styles du document sont mis à jour pour correspondre aux styles du modèle joint chaque fois que le document est ouvert dans MS Word. |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Obtient ou définit la forme d'arrière-plan du document. Peut être`nul` . |
| [Bibliography](../../aspose.words/document/bibliography/) { get; } | Obtient le[`Bibliography`](./bibliography/)objet qui représente la liste des sources disponibles dans le document. |
| [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/) { get; } | Renvoie une collection qui représente toutes les propriétés de document intégrées du document. |
| [CompatibilityOptions](../../aspose.words/document/compatibilityoptions/) { get; } | Donne accès aux options de compatibilité des documents (c'est-à-dire aux préférences utilisateur saisies sur le**Compatibilité** onglet du**Options**dialogue dans Word). |
| [Compliance](../../aspose.words/document/compliance/) { get; } | Obtient la version de conformité OOXML déterminée à partir du contenu du document chargé. N'a de sens que pour les documents OOXML. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtient le nombre d'enfants immédiats de ce nœud. |
| [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/) { get; } | Renvoie une collection qui représente toutes les propriétés de document personnalisées du document. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| [CustomXmlParts](../../aspose.words/document/customxmlparts/) { get; set; } | Obtient ou définit la collection de parties de stockage de données XML personnalisées. |
| [DefaultTabStop](../../aspose.words/document/defaulttabstop/) { get; set; } | Obtient ou définit l'intervalle (en points) entre les taquets de tabulation par défaut. |
| [DigitalSignatures](../../aspose.words/document/digitalsignatures/) { get; } | Obtient la collection de signatures numériques pour ce document et leurs résultats de validation. |
| override [Document](../../aspose.words/documentbase/document/) { get; } | Obtient cette instance. |
| [EndnoteOptions](../../aspose.words/document/endnoteoptions/) { get; } | Fournit des options qui contrôlent la numérotation et le positionnement des notes de fin dans ce document. |
| [FieldOptions](../../aspose.words/document/fieldoptions/) { get; } | Obtient un[`FieldOptions`](../../aspose.words.fields/fieldoptions/) objet qui représente les options permettant de contrôler la gestion des champs dans le document. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtient le premier enfant du nœud. |
| [FirstSection](../../aspose.words/document/firstsection/) { get; } | Obtient la première section du document. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Donne accès aux propriétés des polices utilisées dans ce document. |
| [FontSettings](../../aspose.words/document/fontsettings/) { get; set; } | Obtient ou définit les paramètres de police du document. |
| [FootnoteOptions](../../aspose.words/document/footnoteoptions/) { get; } | Fournit des options qui contrôlent la numérotation et le positionnement des notes de bas de page dans ce document. |
| [FootnoteSeparators](../../aspose.words/documentbase/footnoteseparators/) { get; } | Donne accès aux séparateurs de notes de bas de page/de fin définis dans le document. |
| [Frameset](../../aspose.words/document/frameset/) { get; } | Renvoie un[`Frameset`](./frameset/) instance si ce document représente une page de cadres. |
| [GlossaryDocument](../../aspose.words/document/glossarydocument/) { get; set; } | Obtient ou définit le document de glossaire dans ce document ou modèle. Un document de glossaire est un espace de stockage pour les entrées d'insertion automatique, de correction automatique et de bloc de construction définies dans un document. |
| [GrammarChecked](../../aspose.words/document/grammarchecked/) { get; set; } | Retours`vrai` si le document a été vérifié pour la grammaire. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Retours`vrai` si ce nœud a des nœuds enfants. |
| [HasMacros](../../aspose.words/document/hasmacros/) { get; } | Retours`vrai` si le document contient un projet VBA (macros). |
| [HasRevisions](../../aspose.words/document/hasrevisions/) { get; } | Retours`vrai` si le document comporte des modifications suivies. |
| [HyphenationOptions](../../aspose.words/document/hyphenationoptions/) { get; } | Donne accès aux options de césure du document. |
| [IncludeTextboxesFootnotesEndnotesInStat](../../aspose.words/document/includetextboxesfootnotesendnotesinstat/) { get; set; } | Spécifie s'il faut inclure les zones de texte, les notes de bas de page et les notes de fin dans les statistiques de comptage de mots. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Retours`vrai` car ce nœud peut avoir des nœuds enfants. |
| [JustificationMode](../../aspose.words/document/justificationmode/) { get; set; } | Obtient ou définit l'ajustement de l'espacement des caractères d'un document. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtient le dernier enfant du nœud. |
| [LastSection](../../aspose.words/document/lastsection/) { get; } | Obtient la dernière section du document. |
| [LayoutOptions](../../aspose.words/document/layoutoptions/) { get; } | Obtient un[`LayoutOptions`](../../aspose.words.layout/layoutoptions/) objet qui représente les options permettant de contrôler le processus de mise en page de ce document. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Donne accès au formatage de liste utilisé dans le document. |
| [MailMerge](../../aspose.words/document/mailmerge/) { get; } | Renvoie un[`MailMerge`](../../aspose.words.mailmerging/mailmerge/) objet qui représente la fonctionnalité de publipostage pour le document. |
| [MailMergeSettings](../../aspose.words/document/mailmergesettings/) { get; set; } | Obtient ou définit l'objet qui contient toutes les informations de publipostage pour un document. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Appelé lorsqu'un nœud est inséré ou supprimé dans le document. |
| override [NodeType](../../aspose.words/document/nodetype/) { get; } | RetoursDocument . |
| [OriginalFileName](../../aspose.words/document/originalfilename/) { get; } | Obtient le nom de fichier d'origine du document. |
| [OriginalLoadFormat](../../aspose.words/document/originalloadformat/) { get; } | Obtient le format du document d'origine qui a été chargé dans cet objet. |
| [PackageCustomParts](../../aspose.words/document/packagecustomparts/) { get; set; } | Obtient ou définit la collection de parties personnalisées (contenu arbitraire) qui sont liées au package OOXML à l'aide de « relations inconnues ». |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Obtient ou définit la couleur de page du document. Cette propriété est une version simplifiée de[`BackgroundShape`](../documentbase/backgroundshape/) . |
| [PageCount](../../aspose.words/document/pagecount/) { get; } | Obtient le nombre de pages du document tel que calculé par l'opération de mise en page la plus récente. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [ProtectionType](../../aspose.words/document/protectiontype/) { get; } | Obtient le type de protection de document actuellement actif. |
| [PunctuationKerning](../../aspose.words/document/punctuationkerning/) { get; set; } | Spécifie si le crénage s'applique à la fois au texte latin et à la ponctuation. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un[`Range`](../range/)objet qui représente la partie d'un document contenue dans ce nœud. |
| [RemovePersonalInformation](../../aspose.words/document/removepersonalinformation/) { get; set; } | Obtient ou définit un indicateur indiquant que Microsoft Word supprimera toutes les informations utilisateur des commentaires, des révisions et des propriétés du document lors de l'enregistrement du document. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Permet de contrôler la manière dont les ressources externes sont chargées. |
| [Revisions](../../aspose.words/document/revisions/) { get; } | Obtient une collection de révisions (modifications suivies) qui existent dans ce document. |
| [RevisionsView](../../aspose.words/document/revisionsview/) { get; set; } | Obtient ou définit une valeur indiquant s'il faut travailler avec la version originale ou révisée d'un document. |
| [Sections](../../aspose.words/document/sections/) { get; } | Renvoie une collection qui représente toutes les sections du document. |
| [ShadeFormData](../../aspose.words/document/shadeformdata/) { get; set; } | Spécifie s'il faut activer l'ombrage gris sur les champs de formulaire. |
| [ShowGrammaticalErrors](../../aspose.words/document/showgrammaticalerrors/) { get; set; } | Spécifie s'il faut afficher les erreurs de grammaire dans ce document. |
| [ShowSpellingErrors](../../aspose.words/document/showspellingerrors/) { get; set; } | Spécifie s'il faut afficher les fautes d'orthographe dans ce document. |
| [SpellingChecked](../../aspose.words/document/spellingchecked/) { get; set; } | Retours`vrai` si l'orthographe du document a été vérifiée. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Renvoie une collection de styles définis dans le document. |
| [Theme](../../aspose.words/document/theme/) { get; } | Obtient le[`Theme`](./theme/) objet pour ce document. |
| [TrackRevisions](../../aspose.words/document/trackrevisions/) { get; set; } | Vrai si les modifications sont suivies lorsque ce document est modifié dans Microsoft Word. |
| [Variables](../../aspose.words/document/variables/) { get; } | Renvoie la collection de variables ajoutées à un document ou à un modèle. |
| [VbaProject](../../aspose.words/document/vbaproject/) { get; set; } | Obtient ou définit un[`VbaProject`](./vbaproject/) . |
| [VersionsCount](../../aspose.words/document/versionscount/) { get; } | Obtient le nombre de versions de document qui ont été stockées dans le document DOC. |
| [ViewOptions](../../aspose.words/document/viewoptions/) { get; } | Fournit des options pour contrôler la façon dont le document est affiché dans Microsoft Word. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Appelé lors de diverses procédures de traitement de documents lorsqu'un problème est détecté qui pourrait entraîner une perte de fidélité des données ou du formatage. |
| [Watermark](../../aspose.words/document/watermark/) { get; } | Donne accès au filigrane du document. |
| [WebExtensionTaskPanes](../../aspose.words/document/webextensiontaskpanes/) { get; } | Renvoie une collection qui représente une liste de compléments du volet Office. |
| [WriteProtection](../../aspose.words/document/writeprotection/) { get; } | Donne accès aux options de protection en écriture du document. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words/document/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Accepte un visiteur. |
| [AcceptAllRevisions](../../aspose.words/document/acceptallrevisions/)() | Accepte toutes les modifications suivies dans le document. |
| override [AcceptEnd](../../aspose.words/document/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Accepte un visiteur pour visiter la fin du document. |
| override [AcceptStart](../../aspose.words/document/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Accepte un visiteur pour visiter le début du document. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Ajoute le nœud spécifié à la fin de la liste des nœuds enfants pour ce nœud. |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument)(*Document, [ImportFormatMode](../importformatmode/)*) | Ajoute le document spécifié à la fin de ce document. |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument_1)(*Document, [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Ajoute le document spécifié à la fin de ce document. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup)() | Nettoie les styles et les listes inutilisés du document. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup_1)(*[CleanupOptions](../cleanupoptions/)*) | Nettoie les styles et les listes inutilisés du document en fonction des[`CleanupOptions`](../cleanupoptions/) . |
| [Clone](../../aspose.words/document/clone/#clone)() | Effectue une copie en profondeur du`Document` . |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crée un doublon du nœud. |
| [Compare](../../aspose.words/document/compare/#compare)(*Document, string, DateTime*) | Compare ce document avec un autre document produisant des modifications en fonction du nombre de révisions d'édition et de format[`Revision`](../revision/) . |
| [Compare](../../aspose.words/document/compare/#compare_1)(*Document, string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Compare ce document avec un autre document produisant des modifications sous forme de nombre de révisions d'édition et de format[`Revision`](../revision/) . Permet de spécifier des options de comparaison à l'aide[`CompareOptions`](../../aspose.words.comparing/compareoptions/) . |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate)(*Document*) | Copie les styles du modèle spécifié dans un document. |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate_1)(*string*) | Copie les styles du modèle spécifié dans un document. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crée un navigateur qui peut être utilisé pour parcourir et lire les nœuds. |
| [EnsureMinimum](../../aspose.words/document/ensureminimum/)() | Si le document ne contient aucune section, crée une section avec un paragraphe. |
| [ExpandTableStylesToDirectFormatting](../../aspose.words/document/expandtablestylestodirectformatting/)() | Convertit la mise en forme spécifiée dans les styles de tableau en mise en forme directe sur les tableaux du document. |
| [ExtractPages](../../aspose.words/document/extractpages/)(*int, int*) | Renvoie le`Document` objet représentant une plage de pages spécifiée. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Obtient le premier ancêtre du spécifié[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtient le premier ancêtre du type d'objet spécifié. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Renvoie un Nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Renvoie une collection active de nœuds enfants qui correspondent au type spécifié. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fournit un support pour chaque itération de style sur les nœuds enfants de ce nœud. |
| [GetPageInfo](../../aspose.words/document/getpageinfo/)(*int*) | Obtient la taille de la page, l'orientation et d'autres informations sur une page qui pourraient être utiles pour l'impression ou le rendu. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Obtient le texte de ce nœud et de tous ses enfants. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../node/), bool*) | Importe un nœud d'un autre document vers le document actuel. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../node/), bool, [ImportFormatMode](../importformatmode/)*) | Importe un nœud d'un autre document vers le document actuel avec une option pour contrôler le formatage. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Renvoie l'index du nœud enfant spécifié dans le tableau de nœuds enfants. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Insère le nœud spécifié immédiatement après le nœud de référence spécifié. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Insère le nœud spécifié immédiatement avant le nœud de référence spécifié. |
| [JoinRunsWithSameFormatting](../../aspose.words/document/joinrunswithsameformatting/)() | Les jointures s'exécutent avec le même formatage dans tous les paragraphes du document. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Obtient le nœud suivant selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [NormalizeFieldTypes](../../aspose.words/document/normalizefieldtypes/)() | Modifie les valeurs du type de champ[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) de[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) dans l'ensemble du document afin qu'ils correspondent aux types de champs contenus dans les codes de champ. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Ajoute le nœud spécifié au début de la liste des nœuds enfants pour ce nœud. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Obtient le nœud précédent selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [Print](../../aspose.words/document/print/#print)() | Imprime l'intégralité du document sur l'imprimante par défaut. |
| [Print](../../aspose.words/document/print/#print_1)(*PrinterSettings*) | Imprime le document selon les paramètres d'imprimante spécifiés, à l'aide du contrôleur d'impression standard (sans interface utilisateur). |
| [Print](../../aspose.words/document/print/#print_3)(*string*) | Imprimez l'intégralité du document sur l'imprimante spécifiée, à l'aide du contrôleur d'impression standard (sans interface utilisateur). |
| [Print](../../aspose.words/document/print/#print_2)(*PrinterSettings, string*) | Imprime le document selon les paramètres d'imprimante spécifiés, en utilisant le contrôleur d'impression standard (sans interface utilisateur) et un nom de document. |
| [Protect](../../aspose.words/document/protect/#protect)(*[ProtectionType](../protectiontype/)*) | Protège le document contre les modifications sans modifier le mot de passe existant ou attribue un mot de passe aléatoire. |
| [Protect](../../aspose.words/document/protect/#protect_1)(*[ProtectionType](../protectiontype/), string*) | Protège le document contre les modifications et définit éventuellement un mot de passe de protection. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Supprime tous les nœuds enfants du nœud actuel. |
| [RemoveBlankPages](../../aspose.words/document/removeblankpages/)() | Supprime les pages vierges du document. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Supprime le nœud enfant spécifié. |
| [RemoveExternalSchemaReferences](../../aspose.words/document/removeexternalschemareferences/)() | Supprime les références de schéma XML externes de ce document. |
| [RemoveMacros](../../aspose.words/document/removemacros/)() | Supprime toutes les macros (le projet VBA) ainsi que les barres d'outils et les personnalisations de commandes du document. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Supprime tout[`SmartTag`](../../aspose.words.markup/smarttag/) nœuds descendants du nœud actuel. |
| [RenderToScale](../../aspose.words/document/rendertoscale/)(*int, Graphics, float, float, float*) | Rend une page de document dans unGraphics objet à une échelle spécifiée. |
| [RenderToSize](../../aspose.words/document/rendertosize/)(*int, Graphics, float, float, float, float*) | Rend une page de document dans unGraphics objet à une taille spécifiée. |
| [Save](../../aspose.words/document/save/#save_2)(*string*) | Enregistre le document dans un fichier. Détermine automatiquement le format d'enregistrement à partir de l'extension. |
| [Save](../../aspose.words/document/save/#save)(*Stream, [SaveFormat](../saveformat/)*) | Enregistre le document dans un flux en utilisant le format spécifié. |
| [Save](../../aspose.words/document/save/#save_1)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Enregistre le document dans un flux en utilisant les options d'enregistrement spécifiées. |
| [Save](../../aspose.words/document/save/#save_3)(*string, [SaveFormat](../saveformat/)*) | Enregistre le document dans un fichier au format spécifié. |
| [Save](../../aspose.words/document/save/#save_4)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Enregistre le document dans un fichier en utilisant les options d'enregistrement spécifiées. |
| [Save](../../aspose.words/document/save/#save_5)(*HttpResponse, string, [ContentDisposition](../contentdisposition/), [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Envoie le document au navigateur client. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Sélectionne le premier[`Node`](../node/) qui correspond à l'expression XPath. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions)(*string*) | Commence à marquer automatiquement toutes les modifications ultérieures que vous apportez au document par programmation comme des modifications de révision. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions_1)(*string, DateTime*) | Commence à marquer automatiquement toutes les modifications ultérieures que vous apportez au document par programmation comme des modifications de révision. |
| [StopTrackRevisions](../../aspose.words/document/stoptrackrevisions/)() | Arrête le marquage automatique des modifications du document comme des révisions. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporte le contenu du nœud dans une chaîne en utilisant les options de sauvegarde spécifiées. |
| [UnlinkFields](../../aspose.words/document/unlinkfields/)() | Dissocie les champs dans l'ensemble du document. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect_1)() | Supprime la protection du document quel que soit le mot de passe. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect)(*string*) | Supprime la protection du document si un mot de passe correct est spécifié. |
| [UpdateActualReferenceMarks](../../aspose.words/document/updateactualreferencemarks/)() | Met à jour le[`ActualReferenceMark`](../../aspose.words.notes/footnote/actualreferencemark/) propriété de toutes les notes de bas de page et de fin du document. |
| [UpdateFields](../../aspose.words/document/updatefields/)() | Met à jour les valeurs des champs dans l'ensemble du document. |
| [UpdateListLabels](../../aspose.words/document/updatelistlabels/)() | Met à jour les étiquettes de liste pour tous les éléments de liste du document. |
| [UpdatePageLayout](../../aspose.words/document/updatepagelayout/)() | Reconstruit la mise en page du document. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail)() | Mises à jour[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) du document en utilisant les options par défaut. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail_1)(*[ThumbnailGeneratingOptions](../../aspose.words.rendering/thumbnailgeneratingoptions/)*) | Mises à jour[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) du document selon les options spécifiées. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount)() | Met à jour les propriétés de nombre de mots du document. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount_1)(*bool*) | Met à jour les propriétés de nombre de mots du document, éventuellement mises à jour[`Lines`](../../aspose.words.properties/builtindocumentproperties/lines/) propriété. |

## Remarques

Le`Document` est un objet central de la bibliothèque Aspose.Words.

Pour charger un document existant dans l'un des[`LoadFormat`](../loadformat/) formats, passez un nom de fichier ou un flux dans l'un des`Document` constructeurs. Pour créer un document vierge, appelez le constructeur the sans paramètres.

Utilisez l'une des surcharges de méthode Save pour enregistrer le document dans l'un des [`SaveFormat`](../saveformat/) formats.

Pour dessiner des pages de document directement sur un**Graphique** objet use [`RenderToScale`](./rendertoscale/) ou[`RenderToSize`](./rendertosize/) méthode.

Pour imprimer le document, utilisez l’un des[`Print`](./print/) méthodes.

[`MailMerge`](./mailmerge/)est le moteur de reporting d'Aspose.Words qui permet de remplir rapidement et facilement des rapports conçus dans Microsoft Word avec des données provenant de diverses sources de données. Les données peuvent provenir d'un DataSet, d'une DataTable, d'une DataView, d'un IDataReader ou d'un tableau de valeurs. **Publipostage** parcourra les enregistrements trouvés dans la source de données et les insérera dans les champs de fusion et de publipostage du document en les agrandissant si nécessaire.

`Document` stocke des informations sur l'ensemble du document telles que[`Styles`](../documentbase/styles/) , [`BuiltInDocumentProperties`](./builtindocumentproperties/) ,[`CustomDocumentProperties`](./customdocumentproperties/) , listes et macros. La plupart de ces objets sont accessibles via les propriétés correspondantes du`Document`.

Le`Document` est un nœud racine d'un arbre qui contient tous les autres nœuds du document. L'arbre est un modèle de conception composite et à bien des égards similaire à XmlDocument. Le contenu du document peut être manipulé librement par programmation :

* Les nœuds du document sont accessibles via des collections typées, par exemple[`Sections`](./sections/) , [`ParagraphCollection`](../paragraphcollection/) etc.
* Les nœuds du document peuvent être sélectionnés par leur type de nœud en utilisant [`GetChildNodes`](../compositenode/getchildnodes/) ou en utilisant une requête XPath avec[`SelectNodes`](../compositenode/selectnodes/) ou[`SelectSingleNode`](../compositenode/selectsinglenode/).
* Les nœuds de contenu peuvent être ajoutés ou supprimés de n'importe où dans le document à l'aide de [`InsertBefore`](../compositenode/insertbefore/) ,[`InsertAfter`](../compositenode/insertafter/) , [`RemoveChild`](../compositenode/removechild/) et autres méthodes fournies par la classe de base[`CompositeNode`](../compositenode/).
* Les attributs de formatage de chaque nœud peuvent être modifiés via les propriétés de ce nœud.

Envisagez d'utiliser[`DocumentBuilder`](../documentbuilder/) ce qui simplifie la tâche de création programmatique de x000d ou de remplissage de l'arborescence du document.

Le`Document` ne peut contenir que[`Section`](../section/) objets.

Dans Microsoft Word, un document valide doit comporter au moins une section.

## Exemples

Montre comment exécuter un publipostage avec des données provenant d'un DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Vous trouverez ci-dessous deux manières d'utiliser un DataTable comme source de données pour un publipostage.
    // 1 - Utilisez la table entière pour le publipostage afin de créer un document de publipostage de sortie pour chaque ligne de la table :
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilisez une ligne du tableau pour créer un document de publipostage de sortie :
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Crée un document source de publipostage.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Voir également

* class [DocumentBase](../documentbase/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
