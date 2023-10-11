---
title: Class Document
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Document classe. Représente un document Word.
type: docs
weight: 430
url: /fr/net/aspose.words/document/
---
## Document class

Représente un document Word.

Pour en savoir plus, visitez le[Travailler avec un document](https://docs.aspose.com/words/net/working-with-document/) article documentaire.

```csharp
public class Document : DocumentBase
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [Document](document/#constructor)() | Crée un document Word vierge. |
| [Document](document/#constructor_1)(Stream) | Ouvre un document existant à partir d'un flux. Détecte automatiquement le format de fichier. |
| [Document](document/#constructor_3)(string) | Ouvre un document existant à partir d'un fichier. Détecte automatiquement le format de fichier. |
| [Document](document/#constructor_2)(Stream, LoadOptions) | Ouvre un document existant à partir d'un flux. Permet de spécifier des options supplémentaires telles qu'un mot de passe de cryptage. |
| [Document](document/#constructor_4)(string, LoadOptions) | Ouvre un document existant à partir d'un fichier. Permet de spécifier des options supplémentaires telles qu'un mot de passe de cryptage. |

## Propriétés

| Nom | La description |
| --- | --- |
| [AttachedTemplate](../../aspose.words/document/attachedtemplate/) { get; set; } | Obtient ou définit le chemin complet du modèle joint au document. |
| [AutomaticallyUpdateStyles](../../aspose.words/document/automaticallyupdatestyles/) { get; set; } | Obtient ou définit un indicateur indiquant si les styles du document sont mis à jour pour correspondre aux styles du modèle joint à chaque fois que le document est ouvert dans MS Word. |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Obtient ou définit la forme d'arrière-plan du document. Peut être`nul` . |
| [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/) { get; } | Renvoie une collection qui représente toutes les propriétés de document intégrées du document. |
| [CompatibilityOptions](../../aspose.words/document/compatibilityoptions/) { get; } | Donne accès aux options de compatibilité des documents (c'est-à-dire les préférences utilisateur saisies dans le **Compatibilité** Onglet du **Possibilités** boîte de dialogue dans Word). |
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
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Fournit un accès aux propriétés des polices utilisées dans ce document. |
| [FontSettings](../../aspose.words/document/fontsettings/) { get; set; } | Obtient ou définit les paramètres de police du document. |
| [FootnoteOptions](../../aspose.words/document/footnoteoptions/) { get; } | Fournit des options qui contrôlent la numérotation et le positionnement des notes de bas de page dans ce document. |
| [Frameset](../../aspose.words/document/frameset/) { get; } | Renvoie un[`Frameset`](./frameset/)exemple si ce document représente une page de frames. |
| [GlossaryDocument](../../aspose.words/document/glossarydocument/) { get; set; } | Obtient ou définit le document glossaire dans ce document ou modèle. Un document de glossaire est un stockage pour les entrées AutoText, AutoCorrect et Building Block définies dans un document. |
| [GrammarChecked](../../aspose.words/document/grammarchecked/) { get; set; } | Retours`vrai` si le document a été vérifié pour la grammaire. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Retours`vrai` si ce nœud a des nœuds enfants. |
| [HasMacros](../../aspose.words/document/hasmacros/) { get; } | Retours`vrai` si le document a un projet VBA (macros). |
| [HasRevisions](../../aspose.words/document/hasrevisions/) { get; } | Retours`vrai` si le document comporte des modifications suivies. |
| [HyphenationOptions](../../aspose.words/document/hyphenationoptions/) { get; } | Donne accès aux options de césure des documents. |
| [IncludeTextboxesFootnotesEndnotesInStat](../../aspose.words/document/includetextboxesfootnotesendnotesinstat/) { get; set; } | Spécifie s'il faut inclure des zones de texte, des notes de bas de page et des notes de fin dans les statistiques du nombre de mots. |
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
| [OriginalLoadFormat](../../aspose.words/document/originalloadformat/) { get; } | Obtient le format du document original chargé dans cet objet. |
| [PackageCustomParts](../../aspose.words/document/packagecustomparts/) { get; set; } | Obtient ou définit la collection de parties personnalisées (contenu arbitraire) liées au package OOXML à l'aide de « relations inconnues ». |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Obtient ou définit la couleur de la page du document. Cette propriété est une version plus simple de[`BackgroundShape`](../documentbase/backgroundshape/) . |
| [PageCount](../../aspose.words/document/pagecount/) { get; } | Obtient le nombre de pages du document calculé par l'opération de mise en page la plus récente. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [ProtectionType](../../aspose.words/document/protectiontype/) { get; } | Obtient le type de protection de document actuellement actif. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un[`Range`](../range/) objet qui représente la partie d'un document contenue dans ce nœud. |
| [RemovePersonalInformation](../../aspose.words/document/removepersonalinformation/) { get; set; } | Obtient ou définit un indicateur indiquant que Microsoft Word supprimera toutes les informations utilisateur des commentaires, des révisions et des propriétés du document lors de l'enregistrement du document. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Permet de contrôler la manière dont les ressources externes sont chargées. |
| [Revisions](../../aspose.words/document/revisions/) { get; } | Obtient une collection de révisions (modifications suivies) qui existent dans ce document. |
| [RevisionsView](../../aspose.words/document/revisionsview/) { get; set; } | Obtient ou définit une valeur indiquant s'il faut utiliser la version originale ou révisée d'un document. |
| [Sections](../../aspose.words/document/sections/) { get; } | Renvoie une collection qui représente toutes les sections du document. |
| [ShadeFormData](../../aspose.words/document/shadeformdata/) { get; set; } | Spécifie s'il faut activer l'ombrage gris sur les champs du formulaire. |
| [ShowGrammaticalErrors](../../aspose.words/document/showgrammaticalerrors/) { get; set; } | Spécifie s'il faut afficher les erreurs de grammaire dans ce document. |
| [ShowSpellingErrors](../../aspose.words/document/showspellingerrors/) { get; set; } | Spécifie s'il faut afficher les fautes d'orthographe dans ce document. |
| [SpellingChecked](../../aspose.words/document/spellingchecked/) { get; set; } | Retours`vrai` si l'orthographe du document a été vérifiée. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Renvoie une collection de styles définis dans le document. |
| [Theme](../../aspose.words/document/theme/) { get; } | Obtient le[`Theme`](./theme/) objet pour ce document. |
| [TrackRevisions](../../aspose.words/document/trackrevisions/) { get; set; } | True si les modifications sont suivies lorsque ce document est modifié dans Microsoft Word. |
| [Variables](../../aspose.words/document/variables/) { get; } | Renvoie la collection de variables ajoutées à un document ou un modèle. |
| [VbaProject](../../aspose.words/document/vbaproject/) { get; set; } | Obtient ou définit un[`VbaProject`](./vbaproject/) . |
| [VersionsCount](../../aspose.words/document/versionscount/) { get; } | Obtient le nombre de versions de document stockées dans le document DOC. |
| [ViewOptions](../../aspose.words/document/viewoptions/) { get; } | Fournit des options pour contrôler la façon dont le document est affiché dans Microsoft Word. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Appelé lors de diverses procédures de traitement de documents lorsqu'un problème est détecté qui pourrait entraîner une perte de fidélité des données ou du formatage. |
| [Watermark](../../aspose.words/document/watermark/) { get; } | Donne accès au filigrane du document. |
| [WebExtensionTaskPanes](../../aspose.words/document/webextensiontaskpanes/) { get; } | Renvoie une collection qui représente une liste de compléments du volet Office. |
| [WriteProtection](../../aspose.words/document/writeprotection/) { get; } | Donne accès aux options de protection en écriture du document. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words/document/accept/)(DocumentVisitor) | Accepte un visiteur. |
| [AcceptAllRevisions](../../aspose.words/document/acceptallrevisions/)() | Accepte toutes les modifications suivies dans le document. |
| override [AcceptEnd](../../aspose.words/document/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words/document/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument)(Document, ImportFormatMode) | Ajoute le document spécifié à la fin de ce document. |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument_1)(Document, ImportFormatMode, ImportFormatOptions) | Ajoute le document spécifié à la fin de ce document. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup)() | Nettoie les styles et les listes inutilisés du document. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup_1)(CleanupOptions) | Nettoie les styles et les listes inutilisés du document en fonction des données[`CleanupOptions`](../cleanupoptions/) . |
| [Clone](../../aspose.words/document/clone/#clone)() | Effectue une copie complète du`Document` . |
| [Clone](../../aspose.words/node/clone/)(bool) | Crée un duplicata du nœud. |
| [Compare](../../aspose.words/document/compare/#compare)(Document, string, DateTime) | Compare ce document avec un autre document produisant des modifications en nombre de révisions d'édition et de format[`Revision`](../revision/) . |
| [Compare](../../aspose.words/document/compare/#compare_1)(Document, string, DateTime, CompareOptions) | Compare ce document avec un autre document produisant des changements sous forme d'un certain nombre de révisions d'édition et de format[`Revision`](../revision/) . Permet de spécifier des options de comparaison en utilisant[`CompareOptions`](../../aspose.words.comparing/compareoptions/) . |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate)(Document) | Copie les styles du modèle spécifié vers un document. |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate_1)(string) | Copie les styles du modèle spécifié vers un document. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crée un navigateur qui peut être utilisé pour parcourir et lire des nœuds. |
| [EnsureMinimum](../../aspose.words/document/ensureminimum/)() | Si le document ne contient aucune section, crée une section avec un paragraphe. |
| [ExpandTableStylesToDirectFormatting](../../aspose.words/document/expandtablestylestodirectformatting/)() | Convertit le formatage spécifié dans les styles de tableau en formatage direct sur les tableaux du document. |
| [ExtractPages](../../aspose.words/document/extractpages/)(int, int) | Renvoie le`Document` objet représentant la plage spécifiée de pages. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtient le premier ancêtre du spécifié[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtient le premier ancêtre du type d'objet spécifié. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Renvoie un Nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Renvoie une collection active de nœuds enfants qui correspondent au type spécifié. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fournit la prise en charge de chaque itération de style sur les nœuds enfants de ce nœud. |
| [GetPageInfo](../../aspose.words/document/getpageinfo/)(int) | Obtient la taille de la page, son orientation et d'autres informations sur une page qui pourraient être utiles pour l'impression ou le rendu. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Récupère le texte de ce nœud et de tous ses enfants. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(Node, bool) | Importe un nœud d'un autre document vers le document actuel. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(Node, bool, ImportFormatMode) | Importe un nœud d'un autre document vers le document actuel avec une option pour contrôler le formatage. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Renvoie l'index du nœud enfant spécifié dans le tableau de nœuds enfants. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [JoinRunsWithSameFormatting](../../aspose.words/document/joinrunswithsameformatting/)() | Les jointures s'exécutent avec le même formatage dans tous les paragraphes du document. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtient le nœud suivant selon l'algorithme de traversée de l'arbre de pré-commande. |
| [NormalizeFieldTypes](../../aspose.words/document/normalizefieldtypes/)() | Modifie les valeurs du type de champ[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) de[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) dans tout le document afin qu'ils correspondent aux types de champs contenus dans les codes de champs. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtient le nœud précédent selon l'algorithme de traversée d'arbre de pré-commande. |
| [Print](../../aspose.words/document/print/#print)() | Imprime l'intégralité du document sur l'imprimante par défaut. |
| [Print](../../aspose.words/document/print/#print_1)(PrinterSettings) | Imprime le document selon les paramètres d'imprimante spécifiés, à l'aide du contrôleur d'impression standard (sans interface utilisateur). |
| [Print](../../aspose.words/document/print/#print_3)(string) | Imprimez l'intégralité du document sur l'imprimante spécifiée, à l'aide du contrôleur d'impression standard (sans interface utilisateur). |
| [Print](../../aspose.words/document/print/#print_2)(PrinterSettings, string) | Imprime le document selon les paramètres d'imprimante spécifiés, à l'aide du contrôleur d'impression standard (sans interface utilisateur) et d'un nom de document. |
| [Protect](../../aspose.words/document/protect/#protect)(ProtectionType) | Protège le document des modifications sans modifier le mot de passe existant ou attribue un mot de passe aléatoire. |
| [Protect](../../aspose.words/document/protect/#protect_1)(ProtectionType, string) | Protège le document des modifications et définit éventuellement un mot de passe de protection. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Supprime tous les nœuds enfants du nœud actuel. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveExternalSchemaReferences](../../aspose.words/document/removeexternalschemareferences/)() | Supprime les références de schéma XML externes de ce document. |
| [RemoveMacros](../../aspose.words/document/removemacros/)() | Supprime toutes les macros (le projet VBA) ainsi que les barres d'outils et les personnalisations de commandes du document. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Supprime tout[`SmartTag`](../../aspose.words.markup/smarttag/)nœuds descendants du nœud actuel. |
| [RenderToScale](../../aspose.words/document/rendertoscale/)(int, Graphics, float, float, float) | Rend une page de document dans unGraphics objet à une échelle spécifiée. |
| [RenderToSize](../../aspose.words/document/rendertosize/)(int, Graphics, float, float, float, float) | Rend une page de document dans unGraphics objet à une taille spécifiée. |
| [Save](../../aspose.words/document/save/#save_2)(string) | Enregistre le document dans un fichier. Détermine automatiquement le format de sauvegarde à partir de l'extension. |
| [Save](../../aspose.words/document/save/#save)(Stream, SaveFormat) | Enregistre le document dans un flux en utilisant le format spécifié. |
| [Save](../../aspose.words/document/save/#save_1)(Stream, SaveOptions) | Enregistre le document dans un flux à l'aide des options d'enregistrement spécifiées. |
| [Save](../../aspose.words/document/save/#save_3)(string, SaveFormat) | Enregistre le document dans un fichier au format spécifié. |
| [Save](../../aspose.words/document/save/#save_4)(string, SaveOptions) | Enregistre le document dans un fichier en utilisant les options d'enregistrement spécifiées. |
| [Save](../../aspose.words/document/save/#save_5)(HttpResponse, string, ContentDisposition, SaveOptions) | Envoie le document au navigateur client. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Sélectionne le premier[`Node`](../node/) qui correspond à l'expression XPath. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions)(string) | Commence automatiquement à marquer toutes les autres modifications que vous apportez au document par programme en tant que modifications de révision. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions_1)(string, DateTime) | Commence automatiquement à marquer toutes les autres modifications que vous apportez au document par programme en tant que modifications de révision. |
| [StopTrackRevisions](../../aspose.words/document/stoptrackrevisions/)() | Arrête le marquage automatique des modifications du document en tant que révisions. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporte le contenu du nœud dans une chaîne à l'aide des options de sauvegarde spécifiées. |
| [UnlinkFields](../../aspose.words/document/unlinkfields/)() | Dissocie les champs dans tout le document. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect_1)() | Supprime la protection du document quel que soit le mot de passe. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect)(string) | Supprime la protection du document si un mot de passe correct est spécifié. |
| [UpdateFields](../../aspose.words/document/updatefields/)() | Met à jour les valeurs des champs dans tout le document. |
| [UpdateListLabels](../../aspose.words/document/updatelistlabels/)() | Met à jour les étiquettes de liste pour tous les éléments de liste du document. |
| [UpdatePageLayout](../../aspose.words/document/updatepagelayout/)() | Reconstruit la mise en page du document. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail)() | Mises à jour[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) du document en utilisant les options par défaut. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail_1)(ThumbnailGeneratingOptions) | Mises à jour[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) du document selon les options spécifiées. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount)() | Met à jour les propriétés du nombre de mots du document. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount_1)(bool) | Met à jour les propriétés du nombre de mots du document, éventuellement mises à jour[`Lines`](../../aspose.words.properties/builtindocumentproperties/lines/) propriété. |

### Remarques

Le`Document` est un objet central de la bibliothèque Aspose.Words.

Pour charger un document existant dans l'un des[`LoadFormat`](../loadformat/) formats, transmettez un nom de fichier ou un flux dans l'un des`Document`constructeurs. Pour créer un document vierge, appelez le constructeur sans paramètres.

Utilisez l'une des surcharges de la méthode Save pour enregistrer le document dans l'un des [`SaveFormat`](../saveformat/) formats.

Pour dessiner des pages de document directement sur un **Graphique** objet use [`RenderToScale`](./rendertoscale/) ou[`RenderToSize`](./rendertosize/) méthode.

Pour imprimer le document, utilisez l'un des[`Print`](./print/) méthodes.

[`MailMerge`](./mailmerge/) est le moteur de reporting d'Aspose.Words qui permet de remplir rapidement et facilement des rapports conçus dans Microsoft Word avec des données provenant de diverses sources de données. Les données peuvent provenir d'un DataSet, DataTable, DataView, IDataReader ou d'un tableau de valeurs.  **Fusion et publipostage** parcourra les enregistrements trouvés dans la source de données et les insérera dans les champs de publipostage du document en le développant si nécessaire.

`Document` stocke des informations à l'échelle du document telles que[`Styles`](../documentbase/styles/) , [`BuiltInDocumentProperties`](./builtindocumentproperties/) ,[`CustomDocumentProperties`](./customdocumentproperties/) listes et macros. La plupart de ces objets sont accessibles via les propriétés correspondantes du`Document`.

Le`Document` est un nœud racine d'une arborescence qui contient tous les autres nœuds du document. L'arborescence est un modèle de conception composite et à bien des égards similaire à XmlDocument. Le contenu du document peut être manipulé librement par programme :

* Les nœuds du document sont accessibles via des collections typées, par exemple[`Sections`](./sections/) , [`ParagraphCollection`](../paragraphcollection/) etc.
* Les nœuds du document peuvent être sélectionnés par leur type de nœud en utilisant [`GetChildNodes`](../compositenode/getchildnodes/) ou en utilisant une requête XPath avec[`SelectNodes`](../compositenode/selectnodes/) ou[`SelectSingleNode`](../compositenode/selectsinglenode/).
* Les nœuds de contenu peuvent être ajoutés ou supprimés n'importe où dans le document en utilisant Node) ,Node) , Node) et les méthodes other fournies par la classe de base[`CompositeNode`](../compositenode/).
* Les attributs de formatage de chaque nœud peuvent être modifiés via les propriétés de ce nœud.

Pensez à utiliser[`DocumentBuilder`](../documentbuilder/)cela simplifie la tâche de création par programme de ou de remplissage de l'arborescence des documents.

Le`Document` ne peut contenir que[`Section`](../section/) objets.

Dans Microsoft Word, un document valide doit comporter au moins une section.

### Exemples

Montre comment exécuter un publipostage avec les données d'un DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Vous trouverez ci-dessous deux manières d'utiliser un DataTable comme source de données pour un publipostage.
    // 1 - Utilisez le tableau entier pour le publipostage afin de créer un document de publipostage de sortie pour chaque ligne du tableau :
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilisez une ligne du tableau pour créer un document de publipostage en sortie :
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


